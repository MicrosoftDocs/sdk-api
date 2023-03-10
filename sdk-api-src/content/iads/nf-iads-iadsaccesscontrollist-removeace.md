---
UID: NF:iads.IADsAccessControlList.RemoveAce
title: IADsAccessControlList::RemoveAce (iads.h)
description: Removes an access-control entry (ACE) from the access-control list (ACL).
helpviewer_keywords: ["IADsAccessControlList interface [ADSI]","RemoveAce method","IADsAccessControlList.RemoveAce","IADsAccessControlList::RemoveAce","RemoveAce","RemoveAce method [ADSI]","RemoveAce method [ADSI]","IADsAccessControlList interface","_ds_iadsaccesscontrollist_removeace","adsi.iadsaccesscontrollist__removeace","adsi.iadsaccesscontrollist_removeace","iads/IADsAccessControlList::RemoveAce"]
old-location: adsi\iadsaccesscontrollist_removeace.htm
tech.root: adsi
ms.assetid: 29c1ffcc-5a66-4ee3-889a-747953c604a4
ms.date: 12/05/2018
ms.keywords: IADsAccessControlList interface [ADSI],RemoveAce method, IADsAccessControlList.RemoveAce, IADsAccessControlList::RemoveAce, RemoveAce, RemoveAce method [ADSI], RemoveAce method [ADSI],IADsAccessControlList interface, _ds_iadsaccesscontrollist_removeace, adsi.iadsaccesscontrollist__removeace, adsi.iadsaccesscontrollist_removeace, iads/IADsAccessControlList::RemoveAce
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
 - IADsAccessControlList::RemoveAce
 - iads/IADsAccessControlList::RemoveAce
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
 - IADsAccessControlList.RemoveAce
---

# IADsAccessControlList::RemoveAce


## -description

The <b>IADsAccessControlList::RemoveAce</b> method removes an access-control entry (ACE) from the access-control list (ACL).

## -parameters

### -param pAccessControlEntry [in]

Pointer to the <b>IDispatch</b> interface of the ACE to be removed from the ACL.

## -returns

This method returns standard return values.

For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IADsAccessControlList</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>