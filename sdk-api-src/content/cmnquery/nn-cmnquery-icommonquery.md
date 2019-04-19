---
UID: NN:cmnquery.ICommonQuery
title: ICommonQuery (cmnquery.h)
author: windows-sdk-content
description: Used to programmatically display the system-supplied directory service query dialog box.
old-location: ad\icommonquery.htm
tech.root: ad
ms.assetid: 56d05afb-6e5e-41be-bc10-61192c1c1312
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICommonQuery, ICommonQuery interface [Active Directory], ICommonQuery interface [Active Directory],described, _glines_icommonquery, ad.icommonquery, cmnquery/ICommonQuery
ms.topic: interface
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - ICommonQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICommonQuery interface


## -description


The <b>ICommonQuery</b> interface is used to programmatically display the system-supplied directory service query dialog box.To create an  instance of this interface, call <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> with the <b>CLSID_CommonQuery</b> class identifier as shown in the following code example.

```cpp
HRESULT hr;
ICommonQuery *pCommonQuery;
 
hr = CoCreateInstance(CLSID_CommonQuery,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_ICommonQuery,
    (LPVOID*)&pCommonQuery);
```



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICommonQuery</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICommonQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICommonQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/604c4d7a-1f85-4e5b-9879-be502c5c7bff">OpenQueryWindow</a>
</td>
<td align="left" width="63%">
Displays the directory service query dialog box.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active
    Directory Domain Services</a>
 

 

