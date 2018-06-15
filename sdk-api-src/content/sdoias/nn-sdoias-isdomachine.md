---
UID: NN:sdoias.ISdoMachine
title: ISdoMachine
author: windows-sdk-content
description: Use the ISdoMachine interface to attach to an SDO computer, obtain information about the SDO computer, and obtain interfaces to other SDO objects.
old-location: nps\SDO_isdomachine.htm
old-project: Nps
ms.assetid: 11372116-56eb-4d8e-8f28-4402835ee903
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ISdoMachine, ISdoMachine interface [Network Policy Server], ISdoMachine interface [Network Policy Server],described, _sdo_isdomachine, nps.SDO_isdomachine, sdo.isdomachine, sdoias/ISdoMachine
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VENDORPROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoMachine
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISdoMachine interface


## -description


Use the 
<b>ISdoMachine</b> interface to attach to an SDO computer, obtain information about the SDO computer, and obtain interfaces to other SDO objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISdoMachine</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISdoMachine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISdoMachine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">Attach</a>
</td>
<td align="left" width="63%">
Attaches to a computer in order to administer services on it through SDO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac2fe3e3-a1cb-4642-90af-2b0203e29251">GetAttachedComputer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the currently attached computer, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/172444be-b2a2-4060-af92-b0c63f0ffe6b">GetDictionarySDO</a>
</td>
<td align="left" width="63%">
Retrieves an interface for an attribute-dictionary SDO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c22ec67-4a12-4487-bac5-8f0e666b8029">GetDomainType</a>
</td>
<td align="left" width="63%">
Retrieves the type of domain, if any, in which the SDO computer resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa4f31af-57b0-4ce2-b8b9-981e4ef30d31">GetOSType</a>
</td>
<td align="left" width="63%">
Retrieves the type of operating system running on the SDO computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">GetServiceSDO</a>
</td>
<td align="left" width="63%">
Retrieves an interface for the NPS or for the RAS service SDO.

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c416c0db-836a-4056-bcd7-819f10923446">GetUserSDO</a>
</td>
<td align="left" width="63%">
Retrieves an interface for a user SDO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/733d2911-7e1d-4f73-ae24-1bb748213c1c">IsDirectoryAvailable</a>
</td>
<td align="left" width="63%">
Tests whether an Active Directory service is available on the SDO computer.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/c7b8c59d-91a2-4dfd-a119-ecfd08dcd7aa">Server Data Objects Interfaces</a>



<a href="https://msdn.microsoft.com/0a73adfb-3f4b-46f6-8b76-d48f8599e05d">Server Data Objects Reference</a>
 

 

