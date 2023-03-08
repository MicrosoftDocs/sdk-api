---
UID: NN:iads.IADsMembers
title: IADsMembers (iads.h)
description: The IADsMembers interface is a dual interface.
helpviewer_keywords: ["IADsMembers","IADsMembers interface [ADSI]","IADsMembers interface [ADSI]","described","_ds_iadsmembers","adsi.iadsmembers","iads/IADsMembers"]
old-location: adsi\iadsmembers.htm
tech.root: adsi
ms.assetid: 889e8fc1-61a6-4a3a-82ac-85d41f664149
ms.date: 12/05/2018
ms.keywords: IADsMembers, IADsMembers interface [ADSI], IADsMembers interface [ADSI],described, _ds_iadsmembers, adsi.iadsmembers, iads/IADsMembers
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
 - IADsMembers
 - iads/IADsMembers
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
 - IADsMembers
---

# IADsMembers interface


## -description

The <b>IADsMembers</b> interface is a dual interface. It is designed for managing a list of ADSI object references. It is implemented to support group membership for individual accounts. It can be used to manage a collection of ADSI objects belonging to a group. To access the collection of group members, use the  <a href="/windows/desktop/ADSI/iadsgroup-property-methods">IADsGroup::get_Members</a> property method implemented by the ADSI group object.

The <b>IADsMembers</b> interface serves a slightly different purpose from the  <a href="/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a> and  <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interfaces, which also works with a set of data or objects. <b>IADsCollection</b> manages sets of arbitrary data elements that are not object references, whereas <b>IADsContainer</b> manages objects that are part of the directory tree structure or the network topology.

## -inheritance

The <b>IADsMembers</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsMembers</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/ADSI/iadsgroup-property-methods">IADsGroup::get_Members</a>



<a href="/windows/desktop/ADSI/iadsmembers-property-methods">IADsMembers Property
    Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
