---
UID: NF:iads.IADsUser.Groups
title: IADsUser::Groups (iads.h)
description: Obtains a collection of the ADSI group objects to which this user belongs.
helpviewer_keywords: ["Groups","Groups method [ADSI]","Groups method [ADSI]","IADsUser interface","IADsUser interface [ADSI]","Groups method","IADsUser.Groups","IADsUser::Groups","_ds_iadsuser_groups","adsi.iadsuser__groups","adsi.iadsuser_groups","iads/IADsUser::Groups"]
old-location: adsi\iadsuser_groups.htm
tech.root: adsi
ms.assetid: 0d250815-a7d8-4e61-b125-a66f1c2fde43
ms.date: 12/05/2018
ms.keywords: Groups, Groups method [ADSI], Groups method [ADSI],IADsUser interface, IADsUser interface [ADSI],Groups method, IADsUser.Groups, IADsUser::Groups, _ds_iadsuser_groups, adsi.iadsuser__groups, adsi.iadsuser_groups, iads/IADsUser::Groups
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
 - IADsUser::Groups
 - iads/IADsUser::Groups
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
 - IADsUser.Groups
---

# IADsUser::Groups


## -description

The <b>IADsUser::Groups</b> method obtains a collection of the ADSI group objects to which this user belongs. The method returns an  <a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a> interface pointer through which you can enumerate all the groups in the collection.

## -parameters

### -param ppGroups [out]

Pointer to a pointer to the <a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a> interface on a members object that can be enumerated using  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> to determine the groups to which this end-user belongs.

## -returns

This method supports the standard return values, including S_OK. For other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsuser">IADsUser</a>



<a href="/windows/desktop/ADSI/iadsuser-property-methods">IADsUser
  Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>