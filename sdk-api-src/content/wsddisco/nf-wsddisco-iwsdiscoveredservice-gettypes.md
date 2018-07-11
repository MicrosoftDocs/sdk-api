---
UID: NF:wsddisco.IWSDiscoveredService.GetTypes
title: IWSDiscoveredService::GetTypes
author: windows-sdk-content
description: Retrieves a list of WS-Discovery Types.
old-location: ncd\iwsdiscoveredservice_gettypes.htm
old-project: wsdapi
ms.assetid: fda4def4-4c1d-49a7-bfc1-56ff744a7a9d
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: GetTypes, GetTypes method, GetTypes method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetTypes method, IWSDiscoveredService.GetTypes, IWSDiscoveredService::GetTypes, ncd.iwsdiscoveredservice_gettypes, wsddisco/IWSDiscoveredService::GetTypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveredService.GetTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveredService::GetTypes


## -description


Retrieves a list of WS-Discovery Types.


## -parameters




### -param ppTypesList [in]

List of WS-Discovery Types provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device. For details, see <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a>. Do not deallocate the output structure.


## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppTypesList</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The resulting pointer value is only valid for the lifetime of the <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> object.




## -see-also




<a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>
 

 

