---
UID: NN:imapi2.IDiscMaster2
title: IDiscMaster2 (imapi2.h)
description: Use this interface to enumerate the CD and DVD devices installed on the computer.
helpviewer_keywords: ["IDiscMaster2","IDiscMaster2 interface [IMAPI]","IDiscMaster2 interface [IMAPI]","described","imapi.idiscmaster2","imapi2/IDiscMaster2"]
old-location: imapi\idiscmaster2.htm
tech.root: imapi
ms.assetid: cdca44d4-6ab5-4c2f-91ba-bef79b1d457e
ms.date: 12/05/2018
ms.keywords: IDiscMaster2, IDiscMaster2 interface [IMAPI], IDiscMaster2 interface [IMAPI],described, imapi.idiscmaster2, imapi2/IDiscMaster2
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscMaster2
 - imapi2/IDiscMaster2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscMaster2
---

# IDiscMaster2 interface


## -description

Use this interface to enumerate the CD and DVD devices installed on the computer.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscMaster2) for the class identifier and __uuidof(IDiscMaster2) for the interface identifier.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscMaster2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDiscMaster2</b> also has these types of members:
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
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves a list of the CD and DVD devices installed on the computer.    

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of the CD and DVD disc devices installed on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_issupportedenvironment">get_IsSupportedEnvironment</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines if the environment contains one or more optical devices and the execution context has permission to access the devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier of the specified disc device.

</td>
</tr>
</table>

## -remarks

To create the <b>MsftDiscMaster2</b> object in a script, use IMAPI2.MsftDiscMaster2 as the program identifier when calling <b>CreateObject</b>.

To receive notification when a device is added or removed from the computer, implement the <a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events">DDiscMaster2Events</a> interface.