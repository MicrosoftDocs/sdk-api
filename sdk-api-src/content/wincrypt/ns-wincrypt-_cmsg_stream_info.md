---
UID: NS:wincrypt._CMSG_STREAM_INFO
title: "_CMSG_STREAM_INFO"
author: windows-sdk-content
description: Used to enable stream processing of data rather than single block processing.
old-location: security\cmsg_stream_info.htm
tech.root: seccrypto
ms.assetid: a4e7f6e8-351f-4981-b223-50b65f503394
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PCMSG_STREAM_INFO, CMSG_STREAM_INFO, CMSG_STREAM_INFO structure [Security], PCMSG_STREAM_INFO, PCMSG_STREAM_INFO structure pointer [Security], _CMSG_STREAM_INFO, _crypto2_cmsg_stream_info, cbData, fFinal, pbData, pvArg, security.cmsg_stream_info, wincrypt/CMSG_STREAM_INFO, wincrypt/PCMSG_STREAM_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_STREAM_INFO
product: Windows
targetos: Windows
req.typenames: CMSG_STREAM_INFO, *PCMSG_STREAM_INFO
req.redist: 
---

# _CMSG_STREAM_INFO structure


## -description


The <b>CMSG_STREAM_INFO</b> structure is used to enable stream processing of data rather than single block processing. Stream processing is most often used when processing large messages. Stream-processed messages can originate from any serialized source such as a file on a hard disk, a server, or a CD ROM.

This structure is passed to 
the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> and 
<a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a> functions.


## -struct-fields




### -field cbContent

Specifies the size, in bytes, of the content. Normal <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoding is used unless <b>CMSG_INDEFINITE_LENGTH</b>(0xFFFFFFFF) is passed, indicating that the application is not specifying the content length. This forces the use of indefinite-length <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">Basic Encoding Rules</a> (BER) encoding.


### -field pfnStreamOutput

The address of a callback function used to read from and write data to a disk when processing large messages. 




The callback function must have the following signature and parameters:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;Wincrypt.h&gt;

BOOL WINAPI CmsgStreamOutputCallback(
  IN const void *pvArg,  //in
  IN BYTE *pbData,       //in
  IN DWORD cbData,       //in
  IN BOOL fFinal         //in
);
</pre>
</td>
</tr>
</table></span></div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="pvArg"></a><a id="pvarg"></a><a id="PVARG"></a><dl>
<dt><b>pvArg</b></dt>
</dl>
</td>
<td width="60%">
The arguments specified by CMSG_STREAM_INFO.

</td>
</tr>
<tr>
<td width="40%"><a id="pbData"></a><a id="pbdata"></a><a id="PBDATA"></a><dl>
<dt><b>pbData</b></dt>
</dl>
</td>
<td width="60%">
A pointer to a block of processed data that is available to the application.

</td>
</tr>
<tr>
<td width="40%"><a id="cbData"></a><a id="cbdata"></a><a id="CBDATA"></a><dl>
<dt><b>cbData</b></dt>
</dl>
</td>
<td width="60%">
The size, in bytes, of the block of processed data at pbData.
							

</td>
</tr>
<tr>
<td width="40%"><a id="fFinal"></a><a id="ffinal"></a><a id="FFINAL"></a><dl>
<dt><b>fFinal</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the last block of data is being processed and that this is the last time the callback will be executed.

</td>
</tr>
</table>
 


### -field pvArg

A pointer to the argument to pass to the callback function. Typically, this is used for state data that includes the handle to a more deeply nested message (when decoding) or a less deeply nested message (when encoding).


## -remarks



Messages can be so large that processing them all at once by storing the whole message in memory can be difficult, if not impossible. It is possible to process large messages without encountering memory limitations by streaming the data that is to be processed into manageable sized blocks. The 
<a href="cryptography_functions.htm">low-level message functions</a> can be used with streaming to encode or decode a message. Any level of nesting of messages is supported when streaming to encode and streaming to decode.

The input message to be processed as a stream feeds into 
<a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a> one block at a time, with the application determining the size of the block. As the streamed message is processed for encoding or decoding, the resulting output data is passed back to the application through an application-specified callback function that is specified by the <b>pfnStreamOutput</b> member.

No assumptions can be made about the block size of the output data because the size can vary for several reasons, such as the jitter in output block size caused by the block size for the encryption algorithm when processing an enveloped message, or when blocks that contain the message header and the SignerInfo as defined by PKCS # 7 are processed.

The size of the output block is passed to the callback function in its <i>cbData</i> parameter. The use of output data is determined in the calling application. Typically, output from stream processing will not be persisted in memory as a whole due to memory limitations; rather, it will be serialized to a disk or server file.



