---
UID: NF:msctf.ITfKeystrokeMgr.PreserveKey
title: ITfKeystrokeMgr::PreserveKey
author: windows-sdk-content
description: ITfKeystrokeMgr::PreserveKey method
old-location: tsf\itfkeystrokemgr_preservekey.htm
old-project: TSF
ms.assetid: ad5cd485-9231-4c29-8977-754dbf25c979
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],PreserveKey method, ITfKeystrokeMgr.PreserveKey, ITfKeystrokeMgr::PreserveKey, PreserveKey, PreserveKey method [Text Services Framework], PreserveKey method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_preservekey_ref, msctf/ITfKeystrokeMgr::PreserveKey, tsf.itfkeystrokemgr_preservekey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
 - ITfKeystrokeMgr.PreserveKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeystrokeMgr::PreserveKey


## -description




## -parameters




### -param tid [in]

Contains the client identifier of the TSF text service. This value is passed to the TSF text service in its <a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate</a> method.


### -param rguid [in]

Contains the command GUID of the preserved key. This value is passed to the TSF text service <a href="https://msdn.microsoft.com/90b3f2f4-5655-42e3-bdef-62c090800e5e">ITfKeyEventSink::OnPreservedKey</a> method to identify the preserved key when the preserved key is activated.


### -param prekey [in]

Pointer to a <a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">TF_PRESERVEDKEY</a> structure that specifies the preserved key. The <b>uVKey</b> member contains the virtual key code and the <b>uModifiers</b> member identifies the modifiers of the preserved key.


### -param pchDesc [in]

Pointer to a Unicode string that contains the description of the preserved key. This cannot be <b>NULL</b> unless <i>cchDesc</i> is zero.


### -param cchDesc [in]

Specifies the number of characters in <i>pchDesc</i>. Pass zero for this parameter if no description is required.


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
<dt><b>TF_E_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The preserved key is registered.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

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




<a href="https://msdn.microsoft.com/90b3f2f4-5655-42e3-bdef-62c090800e5e">ITfKeyEventSink::OnPreservedKey
      </a>



<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>



<a href="https://msdn.microsoft.com/05975fce-04c3-4316-a9b2-ed015e7aa8fe">
        ITfKeystrokeMgr::UnpreserveKey
      </a>



<a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">
        ITfTextInputProcessor::Activate
      </a>



<a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">
        TF_PRESERVEDKEY
      </a>
 

 

