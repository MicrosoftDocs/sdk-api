---
UID: NF:msctf.ITfKeystrokeMgr.GetPreservedKey
title: ITfKeystrokeMgr::GetPreservedKey
author: windows-sdk-content
description: ITfKeystrokeMgr::GetPreservedKey method
old-location: tsf\itfkeystrokemgr_getpreservedkey.htm
tech.root: TSF
ms.assetid: d87b3b1c-0e51-4e89-b837-79ed2fe78bbb
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetPreservedKey, GetPreservedKey method [Text Services Framework], GetPreservedKey method [Text Services Framework],ITfKeystrokeMgr interface, ITfKeystrokeMgr interface [Text Services Framework],GetPreservedKey method, ITfKeystrokeMgr.GetPreservedKey, ITfKeystrokeMgr::GetPreservedKey, _tsf_itfkeystrokemgr_getpreservedkey_ref, msctf/ITfKeystrokeMgr::GetPreservedKey, tsf.itfkeystrokemgr_getpreservedkey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeystrokeMgr.GetPreservedKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfKeystrokeMgr.GetPreservedKey
: 
---

# ITfKeystrokeMgr::GetPreservedKey


## -description




## -parameters




### -param pic [in]

Pointer to the application context. This value is returned by a previous call to <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a>.


### -param pprekey [in]

Pointer to a <a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">TF_PRESERVEDKEY</a> structure that identifies the preserved key to obtain. The <b>uVKey</b> member contains the virtual key code and the <b>uModifiers</b> member identifies the modifiers of the preserved key. The <b>uVKey</b> member must be less than 256.


### -param pguid [out]

Pointer to a GUID value that receives the command GUID of the preserved key. This is the GUID passed in the TSF text service call to <a href="https://msdn.microsoft.com/ad5cd485-9231-4c29-8977-754dbf25c979">ITfKeystrokeMgr::PreserveKey</a>. This value receives GUID_NULL if the preserved key is not found.


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
The method was successful and the preserved key was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method was successful, but the preserved key was not found. <i>pguid</i> receives GUID_NULL.

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
</table>
 




## -remarks



Preserved keys are registered by TSF text services and used to provide keyboard shortcuts to common commands implemented by the TSF text service.




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>



<a href="https://msdn.microsoft.com/ad5cd485-9231-4c29-8977-754dbf25c979">ITfKeystrokeMgr::PreserveKey
      </a>



<a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">TF_PRESERVEDKEY
      </a>
 

 

