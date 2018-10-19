---
UID: NF:msctf.ITfDisplayAttributeMgr.GetDisplayAttributeInfo
title: ITfDisplayAttributeMgr::GetDisplayAttributeInfo
author: windows-sdk-content
description: ITfDisplayAttributeMgr::GetDisplayAttributeInfo method
old-location: tsf\itfdisplayattributemgr_getdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: 41bc183f-013f-4e68-bb72-d9a30d5ea48e
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetDisplayAttributeInfo, GetDisplayAttributeInfo method [Text Services Framework], GetDisplayAttributeInfo method [Text Services Framework],ITfDisplayAttributeMgr interface, ITfDisplayAttributeMgr interface [Text Services Framework],GetDisplayAttributeInfo method, ITfDisplayAttributeMgr.GetDisplayAttributeInfo, ITfDisplayAttributeMgr::GetDisplayAttributeInfo, _tsf_itfdisplayattributemgr_getdisplayattributeinfo_ref, msctf/ITfDisplayAttributeMgr::GetDisplayAttributeInfo, tsf.itfdisplayattributemgr_getdisplayattributeinfo
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
 - msctf.dll
api_name:
 - ITfDisplayAttributeMgr.GetDisplayAttributeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfDisplayAttributeMgr::GetDisplayAttributeInfo


## -description




## -parameters




### -param guid [in]

Contains a GUID that identifies the display attribute data requested. This value is obtained by obtaining the GUID_PROP_ATTRIBUTE property for the range of text. For more information, see <a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">ITfContext::GetProperty</a> and <a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">ITfContext::TrackProperties</a>.


### -param ppInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo</a> interface pointer that receives the object.


### -param pclsidOwner [out]

Pointer to a CLSID value that receives the CLSID of the display attribute provider. This parameter can be <b>NULL</b> if the CLSID is not required.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">ITfContext::GetProperty
      </a>



<a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">ITfContext::TrackProperties
      </a>



<a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo
      </a>



<a href="https://msdn.microsoft.com/4a1f9a13-54a1-4294-9635-80eef8bcd8d5">ITfDisplayAttributeMgr</a>
 

 

