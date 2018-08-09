---
UID: NF:ocidl.IClassFactory2.GetLicInfo
title: IClassFactory2::GetLicInfo
author: windows-sdk-content
description: Retrieves information about the licensing capabilities of this class factory.
old-location: com\iclassfactory2_getlicinfo.htm
old-project: com
ms.assetid: e55d1089-b1df-4de0-9a19-cbd255b36126
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetLicInfo, GetLicInfo method [COM], GetLicInfo method [COM],IClassFactory2 interface, IClassFactory2 interface [COM],GetLicInfo method, IClassFactory2.GetLicInfo, IClassFactory2::GetLicInfo, _com_iclassfactory2_getlicinfo, com.iclassfactory2_getlicinfo, ocidl/IClassFactory2::GetLicInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IClassFactory2.GetLicInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IClassFactory2::GetLicInfo


## -description


Retrieves information about the licensing capabilities of this class factory.


## -parameters




### -param pLicInfo [in, out]

A pointer to the caller-allocated <a href="https://msdn.microsoft.com/a90d82f3-8dc4-4b1d-81f7-9d3a19e74314">LICINFO</a> structure to be filled on output.


## -returns



This method can return the standard return values E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/a90d82f3-8dc4-4b1d-81f7-9d3a19e74314">LICINFO</a> structure was successfully filled in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pLicInfo</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not allowed as a return value because this method provides critical information for the client of a licensed class factory.




## -see-also




<a href="https://msdn.microsoft.com/c49c7612-3b1f-4535-baf3-8458b3f34f95">IClassFactory2</a>



<a href="https://msdn.microsoft.com/a90d82f3-8dc4-4b1d-81f7-9d3a19e74314">LICINFO</a>
 

 

