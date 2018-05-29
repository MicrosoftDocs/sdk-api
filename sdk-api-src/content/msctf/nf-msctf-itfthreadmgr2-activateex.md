---
UID: NF:msctf.ITfThreadMgr2.ActivateEx
title: ITfThreadMgr2::ActivateEx
author: windows-sdk-content
description: Initializes and activates TSF for the calling thread with a flag that specifies how TSF is activated.
old-location: tsf\itfthreadmgr2_activateex.htm
old-project: TSF
ms.assetid: 0ADA34C7-6BE8-4719-B220-1F0E5F466178
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ActivateEx, ActivateEx method [Text Services Framework], ActivateEx method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],ActivateEx method, ITfThreadMgr2.ActivateEx, ITfThreadMgr2::ActivateEx, TF_TMAE_COMLESS, TF_TMAE_NOACTIVATEKEYBOARDLAYOUT, TF_TMAE_NOACTIVATETIP, TF_TMAE_SECUREMODE, TF_TMAE_UIELEMENTENABLEDONLY, msctf/ITfThreadMgr2::ActivateEx, tsf.itfthreadmgr2_activateex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.h
api_name:
-	ITfThreadMgr2.ActivateEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgr2::ActivateEx


## -description


Initializes and activates TSF for the calling thread with a flag that specifies how TSF is activated.


## -parameters




### -param ptid [out]

[out] Pointer to a <a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId</a> value that receives a client identifier.


### -param dwFlags [in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_NOACTIVATETIP"></a><a id="tf_tmae_noactivatetip"></a><dl>
<dt><b>TF_TMAE_NOACTIVATETIP</b></dt>
</dl>
</td>
<td width="60%">
Text services will not be activated while this method is called. They will be activated when the calling thread has focus asynchronously.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_SECUREMODE"></a><a id="tf_tmae_securemode"></a><dl>
<dt><b>TF_TMAE_SECUREMODE</b></dt>
</dl>
</td>
<td width="60%">
TSF is activated in secure mode. Only text services that support the secure mode will be activated.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_UIELEMENTENABLEDONLY"></a><a id="tf_tmae_uielementenabledonly"></a><dl>
<dt><b>TF_TMAE_UIELEMENTENABLEDONLY</b></dt>
</dl>
</td>
<td width="60%">
TSF activates only text services that are categorized in GUID_TFCAT_TIPCAP_UIELEMENTENABLED.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_COMLESS"></a><a id="tf_tmae_comless"></a><dl>
<dt><b>TF_TMAE_COMLESS</b></dt>
</dl>
</td>
<td width="60%">
TSF does not use COM. TSF activate only text services that are categorized in GUID_TFCAT_TIPCAP_COMLESS.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_NOACTIVATEKEYBOARDLAYOUT"></a><a id="tf_tmae_noactivatekeyboardlayout"></a><dl>
<dt><b>TF_TMAE_NOACTIVATEKEYBOARDLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
TSF does not sync the current keyboard layout while this method is called. The keyboard layout will be adjusted when the calling thread gets focus. This flag must be used with TF_TMAE_NOACTIVATETIP.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 

