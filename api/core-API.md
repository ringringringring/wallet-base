```javascript

/**
 * 生成助记词
 * @method mnemonic
 * @for Base
 * @param {void}
 * @return {string} 12个助记词
 */
Client.mnemonic()


/**
 * 根据助记词生成根私钥
 * @method xPrivKey
 * @for Base
 * @param {string}  助记词
 * @return {string} 私钥
 */
Client.xPrivKey(mnemonic)


/**
 * 生成根公钥
 * @method xPubKey
 * @for Base
 * @param {string}  根私钥
 * @return {string} 根公钥
 */
Client.xPubKey(xPrivKey)


/**
 * 生成钱包公钥
 * @method walletPubKey
 * @for Base
 * @param {string}  私钥
 * @param {int}     钱包index 0-
 * @return {string} 钱包公钥
 */
Client.walletPubKey(xPrivKey, num)


/**
 * 生成钱包ID
 * @method walletID
 * @for Base
 * @param {string}  钱包公钥
 * @return {string} 钱包ID
 */
Client.walletID(walletPubKey)

/**
 * 生成ecdsa签名公钥
 * @method ecdsaPubkey
 * @for Base
 * @param {string}  根私钥 or 临时私钥。
 *                  若传递根私钥，则必须传递path派生路径；
 *                  若传递临时私钥，则path需要传递字符串null；
 * @param {string}  派生路径
 * @return {string} 签名公钥
 */
Client.ecdsaPubkey(xPrivKey, path)

/**
 * 生成设备地址
 * @method deviceAddress
 * @for Base
 * @param {string}  根私钥
 * @return {string} 设备地址
 */
Client.deviceAddress(xPrivKey)

/**
 * 生成钱包的地址
 * @method walletAddress
 * @for Base
 * @param {string}  钱包公钥
 * @param {int}     收款地址为 0; 找零地址为 1;
 * @param {int}     地址index 0-
 * @return {string} 钱包地址
 */
Client.walletAddress(wallet_xPubKey, change, num)

/**
 * 生成钱包地址对应的公钥
 * @method walletAddressPubkey
 * @for Base
 * @param {string}  钱包公钥
 * @param {int}     收款地址为 0; 找零地址为 1;
 * @param {int}     地址index 0-
 * @return {string} 钱包地址对应的公钥
 */
Clien.walletAddressPubkey(wallet_xPubKey, change, num)

/**
 * 签名
 * @method sign
 * @for Base
 * @param {string}  base64编码过的hash
 * @param {string}  根私钥 or 临时私钥。
 *                  若传递根私钥，则必须传递path派生路径；
 *                  若传递临时私钥，则path需要传递字符串null；
 * @param {string}  派生路径
 * @return {string} 签名结果
 */
Client.sign(b64_hash, xPrivKey, path)

/**
 * 验证签名
 * @method verify
 * @for Base
 * @param {string}  base64编码过的hash
 * @param {string}  签名信息
 * @param {string}  派生公钥
 * @return {bool}   验签结果
 */
Client.verify(b64_hash, sig, pub_key)

/**
 * 生成m/1'私钥
 * @method m1PrivKey
 * @for Base
 * @param {string}  根私钥
 * @return {string} base64编码的私钥
 */
Client.m1PrivKey(xPrivKey)

/**
 * 生成临时私钥
 * @method genPrivKey
 * @for Base
 * @param {void}
 * @return {string} base64编码的私钥
 */
Client.genPrivKey()

/**
 * 根据临时私钥生成临时公钥
 * @method genPubKey
 * @for Base
 * @param {string}  临时私钥
 * @return {string} 临时公钥
 */
Client.genPubKey(privKey)

/**
 * 获得设备消息hash
 * @method getDeviceMessageHashToSign
 * @for Base
 * @param {string}  消息JSON字符串
 * @return {string} base64过的hash
 */
Client.getDeviceMessageHashToSign(unit)

/**
 * 获得交易单元unit hash
 * @method getUnitHash
 * @for Base
 * @param {string}  消息JSON字符串
 * @return {string} base64过的hash
 */
Client.getUnitHash(unit)

/**
 * 获得交易单元待签名hash
 * @method getUnitHashToSign
 * @for Base
 * @param {string}  单元JSON字符串
 * @return {string} base64过的hash
 */
Client.getUnitHashToSign(unit)

/**
 * 获得base64hash
 * @method getBase64Hash
 * @for Base
 * @param {string}  单元JSON字符串
 * @return {string} base64过的hash
 */
Client.getBase64Hash(unit)

/**
 * 获得消息头字节数
 * @method getHeadersSize
 * @for Base
 * @param {string}  单元JSON字符串
 * @return {int}    字节数
 */
Client.getHeadersSize(unit);

/**
 * 获得payload字节数
 * @method getTotalPayloadSize
 * @for Base
 * @param {string}  单元JSON字符串
 * @return {int}    字节数
 */
Client.getTotalPayloadSize(unit);

/**
 * 生成随机字节数
 * @method randomBytes
 * @for Base
 * @param {int}     字节数
 * @return {string} 随机数的base64
 */
Client.randomBytes(num);

/**
 * 验证地址有效性
 * @method isValidAddress
 * @for Base
 * @param {string}  地址字符串
 * @return {bool}   验签结果
 */
Client.isValidAddress(address);

```