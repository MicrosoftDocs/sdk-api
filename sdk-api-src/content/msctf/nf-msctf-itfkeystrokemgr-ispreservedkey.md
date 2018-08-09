---
UID: NF:msctf.ITfKeystrokeMgr.IsPreservedKey
title: ITfKeystrokeMgr::IsPreservedKey
author: windows-sdk-content
description: ITfKeystrokeMgr::IsPreservedKey method
old-location: tsf\itfkeystrokemgr_ispreservedkey.htm
old-project: TSF
ms.assetid: 50deac9c-b659-494b-9cda-d6109fa39363
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],IsPreservedKey method, ITfKeystrokeMgr.IsPreservedKey, ITfKeystrokeMgr::IsPreservedKey, IsPreservedKey, IsPreservedKey method [Text Services Framework], IsPreservedKey method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_ispreservedkey_ref, msctf/ITfKeystrokeMgr::IsPreservedKey, tsf.itfkeystrokemgr_ispreservedkey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeystrokeMgr.IsPreservedKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeystrokeMgr::IsPreservedKey


## -description




## -parameters




### -param rguid [in]

Specifies the command GUID of the preserved key. This is the GUID passed in the text service call to <a href="https://msdn.microsoft.com/ad5cd485-9231-4c29-8977-754dbf25c979">ITfKeystrokeMgr::PreserveKey</a>.


### -param pprekey [in]

Pointer to a <a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">TF_PRESERVEDKEY</a> structure that identifies the preserved key. The <b>uVKey</b> member contains the virtual key code and the <b>uModifiers</b> member identifies the modifiers of the preserved key. The <b>uVKey</b> member must be less than 256.


### -param pfRegistered [out]

Pointer to a BOOL that receives <b>TRUE</b> if the command GUID and key combination is a registered preserved key, or <b>FALSE</b> otherwise.


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
The method was successful, but the preserved key was not found.

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



Preserved keys are registered by TSF text services and provide keyboard shortcuts to common commands implemented by the TSF text service.




## -see-also




<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>



<a href="https://msdn.microsoft.com/ad5cd485-9231-4c29-8977-754dbf25c979">ITfKeystrokeMgr::PreserveKey
      </a>



<a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">TF_PRESERVEDKEY
      </a>
 

 

