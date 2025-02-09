
<a name="0x2_address"></a>

# Module `0x2::address`



-  [Constants](#@Constants_0)
-  [Function `to_u256`](#0x2_address_to_u256)
-  [Function `from_u256`](#0x2_address_from_u256)
-  [Function `from_bytes`](#0x2_address_from_bytes)
-  [Function `to_bytes`](#0x2_address_to_bytes)
-  [Function `to_ascii_string`](#0x2_address_to_ascii_string)
-  [Function `to_string`](#0x2_address_to_string)
-  [Function `length`](#0x2_address_length)
-  [Function `max`](#0x2_address_max)


<pre><code><b>use</b> <a href="../../dependencies/move-stdlib/ascii.md#0x1_ascii">0x1::ascii</a>;
<b>use</b> <a href="../../dependencies/move-stdlib/bcs.md#0x1_bcs">0x1::bcs</a>;
<b>use</b> <a href="../../dependencies/move-stdlib/string.md#0x1_string">0x1::string</a>;
<b>use</b> <a href="../../dependencies/sui-framework/hex.md#0x2_hex">0x2::hex</a>;
</code></pre>



<a name="@Constants_0"></a>

## Constants


<a name="0x2_address_EAddressParseError"></a>



<pre><code><b>const</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_EAddressParseError">EAddressParseError</a>: u64 = 0;
</code></pre>



<a name="0x2_address_LENGTH"></a>



<pre><code><b>const</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_LENGTH">LENGTH</a>: u64 = 32;
</code></pre>



<a name="0x2_address_MAX"></a>



<pre><code><b>const</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_MAX">MAX</a>: u256 = 115792089237316195423570985008687907853269984665640564039457584007913129639935;
</code></pre>



<a name="0x2_address_to_u256"></a>

## Function `to_u256`



<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_to_u256">to_u256</a>(a: <b>address</b>): u256
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_to_u256">to_u256</a>(a: <b>address</b>): u256;
</code></pre>



</details>

<a name="0x2_address_from_u256"></a>

## Function `from_u256`



<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_from_u256">from_u256</a>(n: u256): <b>address</b>
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_from_u256">from_u256</a>(n: u256): <b>address</b>;
</code></pre>



</details>

<a name="0x2_address_from_bytes"></a>

## Function `from_bytes`



<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_from_bytes">from_bytes</a>(bytes: <a href="../../dependencies/move-stdlib/vector.md#0x1_vector">vector</a>&lt;u8&gt;): <b>address</b>
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>native</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_from_bytes">from_bytes</a>(bytes: <a href="../../dependencies/move-stdlib/vector.md#0x1_vector">vector</a>&lt;u8&gt;): <b>address</b>;
</code></pre>



</details>

<a name="0x2_address_to_bytes"></a>

## Function `to_bytes`



<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_to_bytes">to_bytes</a>(a: <b>address</b>): <a href="../../dependencies/move-stdlib/vector.md#0x1_vector">vector</a>&lt;u8&gt;
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_to_bytes">to_bytes</a>(a: <b>address</b>): <a href="../../dependencies/move-stdlib/vector.md#0x1_vector">vector</a>&lt;u8&gt; {
    <a href="../../dependencies/move-stdlib/bcs.md#0x1_bcs_to_bytes">bcs::to_bytes</a>(&a)
}
</code></pre>



</details>

<a name="0x2_address_to_ascii_string"></a>

## Function `to_ascii_string`



<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_to_ascii_string">to_ascii_string</a>(a: <b>address</b>): <a href="../../dependencies/move-stdlib/ascii.md#0x1_ascii_String">ascii::String</a>
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_to_ascii_string">to_ascii_string</a>(a: <b>address</b>): <a href="../../dependencies/move-stdlib/ascii.md#0x1_ascii_String">ascii::String</a> {
    <a href="../../dependencies/move-stdlib/ascii.md#0x1_ascii_string">ascii::string</a>(<a href="../../dependencies/sui-framework/hex.md#0x2_hex_encode">hex::encode</a>(<a href="../../dependencies/sui-framework/address.md#0x2_address_to_bytes">to_bytes</a>(a)))
}
</code></pre>



</details>

<a name="0x2_address_to_string"></a>

## Function `to_string`



<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_to_string">to_string</a>(a: <b>address</b>): <a href="../../dependencies/move-stdlib/string.md#0x1_string_String">string::String</a>
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_to_string">to_string</a>(a: <b>address</b>): <a href="../../dependencies/move-stdlib/string.md#0x1_string_String">string::String</a> {
    <a href="../../dependencies/move-stdlib/string.md#0x1_string_from_ascii">string::from_ascii</a>(<a href="../../dependencies/sui-framework/address.md#0x2_address_to_ascii_string">to_ascii_string</a>(a))
}
</code></pre>



</details>

<a name="0x2_address_length"></a>

## Function `length`



<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_length">length</a>(): u64
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_length">length</a>(): u64 {
    <a href="../../dependencies/sui-framework/address.md#0x2_address_LENGTH">LENGTH</a>
}
</code></pre>



</details>

<a name="0x2_address_max"></a>

## Function `max`



<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_max">max</a>(): u256
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>public</b> <b>fun</b> <a href="../../dependencies/sui-framework/address.md#0x2_address_max">max</a>(): u256 {
    <a href="../../dependencies/sui-framework/address.md#0x2_address_MAX">MAX</a>
}
</code></pre>



</details>
