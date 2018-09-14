---
UID: NF:xenroll.IEnroll4.GetKeyLenEx
title: IEnroll4::GetKeyLenEx
author: windows-sdk-content
description: Retrieves size information for the signature and exchange keys.
old-location: security\ienroll4_getkeylenex.htm
tech.root: seccrypto
ms.assetid: 377fed60-7c04-41c1-bc3d-6567d7d8c389
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetKeyLenEx, GetKeyLenEx method [Security], GetKeyLenEx method [Security],IEnroll4 interface, IEnroll4 interface [Security],GetKeyLenEx method, IEnroll4.GetKeyLenEx, IEnroll4::GetKeyLenEx, XEKL_KEYSIZE_INC, XEKL_KEYSIZE_MAX, XEKL_KEYSIZE_MIN, XEKL_KEYSPEC_KEYX, XEKL_KEYSPEC_SIG, security.ienroll4_getkeylenex, xenroll/IEnroll4::GetKeyLenEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.GetKeyLenEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll4::GetKeyLenEx


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetKeyLenEx</b> method retrieves size information for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signature</a> and <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange keys</a>. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.

The values retrieved by this method are dependent upon the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a>.


## -parameters




### -param lSizeSpec [in]

Value indicating the type of size information to be retrieved. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_MIN"></a><a id="xekl_keysize_min"></a><dl>
<dt><b>XEKL_KEYSIZE_MIN</b></dt>
</dl>
</td>
<td width="60%">
Minimum key size.

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_MAX"></a><a id="xekl_keysize_max"></a><dl>
<dt><b>XEKL_KEYSIZE_MAX</b></dt>
</dl>
</td>
<td width="60%">
Maximum key size.

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_INC"></a><a id="xekl_keysize_inc"></a><dl>
<dt><b>XEKL_KEYSIZE_INC</b></dt>
</dl>
</td>
<td width="60%">
Size of key increment. For more information, see Remarks.

</td>
</tr>
</table>
 


### -param lKeySpec [in]

Specifies the key for which size information is returned. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSPEC_KEYX"></a><a id="xekl_keyspec_keyx"></a><dl>
<dt><b>XEKL_KEYSPEC_KEYX</b></dt>
</dl>
</td>
<td width="60%">
Exchange key

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSPEC_SIG"></a><a id="xekl_keyspec_sig"></a><dl>
<dt><b>XEKL_KEYSPEC_SIG</b></dt>
</dl>
</td>
<td width="60%">
Signature key

</td>
</tr>
</table>
 


### -param pdwKeySize [out]

A pointer to <b>LONG</b> that receives the key size information, in bits.


## -remarks



If the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> does not support this method, an error is returned.

For additional details on the XEKL_KEYSIZE_INC value, see PP_SIG_KEYSIZE_INC usage in the 
<a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a> reference page.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

