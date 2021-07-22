---
UID: NN:iads.IADsCollection
title: IADsCollection (iads.h)
description: The IADsCollection interface is a dual interface that enables its hosting ADSI object to define and manage an arbitrary set of named data elements for a directory service.
helpviewer_keywords: ["IADsCollection","IADsCollection interface [ADSI]","IADsCollection interface [ADSI]","described","_ds_iadscollection","adsi.iadscollection","iads/IADsCollection"]
old-location: adsi\iadscollection.htm
tech.root: adsi
ms.assetid: 4552552b-c008-439a-95bf-eaf9ffd28b5f
ms.date: 12/05/2018
ms.keywords: IADsCollection, IADsCollection interface [ADSI], IADsCollection interface [ADSI],described, _ds_iadscollection, adsi.iadscollection, iads/IADsCollection
req.header: iads.h
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsCollection
 - iads/IADsCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsCollection
---

# IADsCollection interface


## -description

The <b>IADsCollection</b> interface is a dual interface that enables its hosting ADSI object to define and manage an arbitrary set of named data elements for a directory service. Collections differ from arrays of elements in that individual items can be added or deleted without reordering the entire array.

Collection objects can represent one or more items that correspond to volatile data, such as processes or active communication sessions, as well as persistent data, such as physical entities for a directory service. For example, a collection object can represent a list of print jobs in a queue or a list of active sessions connected to a server. Although a collection object can represent arbitrary data sets, all elements in a collection must be of the same type. The data are of <b>Variant</b> types.

ADSI also exposes the  <a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a> and  <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interfaces for manipulating two special cases of collection objects. <b>IADsMembers</b> is used for a collection of objects that share a common membership. An example of such objects are users that belong to a group. <b>IADsContainer</b> applies to an ADSI object that contains other objects. An example of this is a directory tree or a network topology.

## -inheritance

The <b>IADsCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsCollection</b> also has these types of members:

## -remarks

Of the ADSI system providers, only the WinNT provider supports this interface to handle active file service sessions, resources and print jobs.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
