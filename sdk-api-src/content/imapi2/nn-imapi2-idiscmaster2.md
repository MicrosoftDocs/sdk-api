---
UID: NN:imapi2.IDiscMaster2
title: IDiscMaster2
author: windows-driver-content
description: Use this interface to enumerate the CD and DVD devices installed on the computer.
old-location: imapi\idiscmaster2.htm
old-project: imapi
ms.assetid: cdca44d4-6ab5-4c2f-91ba-bef79b1d457e
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IDiscMaster2, IDiscMaster2 interface [IMAPI], IDiscMaster2 interface [IMAPI],described, imapi.idiscmaster2, imapi2/IDiscMaster2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscMaster2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMaster2 interface


## -description


Use this interface to enumerate the CD and DVD devices installed on the computer.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscMaster2) for the class identifier and __uuidof(IDiscMaster2) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscMaster2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IDiscMaster2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscMaster2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f148a1c0-cb76-40e9-9749-a074f04c93e8">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves a list of the CD and DVD devices installed on the computer.    

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1e0ec8f-4c66-4648-ad76-2998200ea574">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of the CD and DVD disc devices installed on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abaa4d89-07b2-4e7a-a0c9-8a31abfd9dd0">get_IsSupportedEnvironment</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines if the environment contains one or more optical devices and the execution context has permission to access the devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e909acb9-850b-404d-a2f7-efb37faf3506">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier of the specified disc device.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftDiscMaster2</b> object in a script, use IMAPI2.MsftDiscMaster2 as the program identifier when calling <b>CreateObject</b>.

To receive notification when a device is added or removed from the computer, implement the <a href="https://msdn.microsoft.com/f01fa2d8-989d-499f-b79d-495108640aa2">DDiscMaster2Events</a> interface.



