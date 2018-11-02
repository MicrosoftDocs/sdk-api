---
UID: NN:msp.ITMSPAddress
title: ITMSPAddress
author: windows-sdk-content
description: The ITMSPAddress interface is implemented by the MSP and represents a media service provider to the TAPI DLL. It is not exposed to end-user or server applications. TAPI 3 will call CoCreateInstance on this interface to create the MSP object.
old-location: tapi3\itmspaddress.htm
tech.root: tapi
ms.assetid: 246a0bcd-0dbb-4b77-a1cd-e6378eaff889
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITMSPAddress, ITMSPAddress interface [TAPI 2.2], ITMSPAddress interface [TAPI 2.2],described, _tapi3_itmspaddress, msp/ITMSPAddress, tapi3.itmspaddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msp.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msp.h
api_name:
 - ITMSPAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMSPAddress interface


## -description


The 
<b>ITMSPAddress</b> interface is implemented by the MSP and represents a media service provider to the TAPI DLL. It is not exposed to end-user or server applications. TAPI 3 will call <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> on this interface to create the MSP object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMSPAddress</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITMSPAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITMSPAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>
</td>
<td align="left" width="63%">
Create an 
<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a> object representing a new TAPI call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">GetEvent</a>
</td>
<td align="left" width="63%">
Gets event information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5df2c486-0133-4705-8d37-10b56b40c85d">Initialize</a>
</td>
<td align="left" width="63%">
Called when the MSP is loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80b8e0aa-3361-4593-bec0-cbe9186c6c41">ReceiveTSPData</a>
</td>
<td align="left" width="63%">
Called when the TSP sends asynchronous data to the MSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/877691cb-b12b-4389-b93c-4ff13a52f4d7">Shutdown</a>
</td>
<td align="left" width="63%">
Called when the MSP is unloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6527db85-cad8-4b0d-977a-9ab8b047e44e">ShutdownMSPCall</a>
</td>
<td align="left" width="63%">
Called when the call is being disconnected.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/17c5f2ba-d526-4b00-9649-8fd73d70bc79">ITSubStreamControl</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

