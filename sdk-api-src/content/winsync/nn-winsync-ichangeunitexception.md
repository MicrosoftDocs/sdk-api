---
UID: NN:winsync.IChangeUnitException
title: IChangeUnitException
author: windows-sdk-content
description: Represents a change unit to exclude from a knowledge object.
old-location: winsync\ichangeunitexception.htm
tech.root: winsync
ms.assetid: 3b47abab-0a33-405f-a765-307ab800bad6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IChangeUnitException, IChangeUnitException interface [Windows Sync], IChangeUnitException interface [Windows Sync],described, winsync.ichangeunitexception, winsync/IChangeUnitException
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - winsync.h
api_name:
 - IChangeUnitException
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IChangeUnitException interface


## -description


Represents a change unit to exclude from a knowledge object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IChangeUnitException</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IChangeUnitException</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IChangeUnitException</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25a6eed2-6851-4a24-afd2-91982dc2bb8e">GetChangeUnitId</a>
</td>
<td align="left" width="63%">
Gets the change unit ID for the change unit that is associated with the exception.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cf95acf-23ab-49c8-bd63-7aff9bad8f25">GetClockVector</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with this exception.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5c76ecf-bd3f-4a0a-9fba-4fd51591d39f">GetItemId</a>
</td>
<td align="left" width="63%">
Gets the item ID for the item that contains the change unit that is associated with the exception.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

