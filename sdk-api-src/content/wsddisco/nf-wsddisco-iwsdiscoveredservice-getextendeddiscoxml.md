---
UID: NF:wsddisco.IWSDiscoveredService.GetExtendedDiscoXML
title: IWSDiscoveredService::GetExtendedDiscoXML
author: windows-sdk-content
description: Retrieves custom or extensible data provided in the header or body of the SOAP message.
old-location: ncd\iwsdiscoveredservice_getextendeddiscoxml.htm
tech.root: WsdApi
ms.assetid: 6ca12b1b-4adf-4c54-90b5-ab5286af9252
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetExtendedDiscoXML, GetExtendedDiscoXML method, GetExtendedDiscoXML method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetExtendedDiscoXML method, IWSDiscoveredService.GetExtendedDiscoXML, IWSDiscoveredService::GetExtendedDiscoXML, ncd.iwsdiscoveredservice_getextendeddiscoxml, wsddisco/IWSDiscoveredService::GetExtendedDiscoXML
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveredService.GetExtendedDiscoXML
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDiscoveredService::GetExtendedDiscoXML


## -description


Retrieves custom or extensible data provided in the header or body of the SOAP message. 


## -parameters




### -param ppHeaderAny [out]

Custom data added to the header portion of the SOAP message. For details, see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a>. Do not deallocate the output structure.


### -param ppBodyAny [out]

Custom data added to the body portion of the SOAP message. For details, see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a>. Do not deallocate the output structure.


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
</table>
 




## -remarks



Some devices may add custom data to the header and body portions of the SOAP message to convey additional information in the discovery phase.

The resulting pointer values are  only valid for the lifetime of the <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> object.




## -see-also




<a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>
 

 

