---
UID: NF:gpedit.IGroupPolicyObject.GetPropertySheetPages
title: IGroupPolicyObject::GetPropertySheetPages (gpedit.h)
description: The GetPropertySheetPages method retrieves the property sheet pages associated with the GPO.
helpviewer_keywords: ["GetPropertySheetPages","GetPropertySheetPages method [Group Policy]","GetPropertySheetPages method [Group Policy]","IGroupPolicyObject interface","IGroupPolicyObject interface [Group Policy]","GetPropertySheetPages method","IGroupPolicyObject.GetPropertySheetPages","IGroupPolicyObject::GetPropertySheetPages","_win32_igrouppolicyobject_getpropertysheetpages","gpedit/IGroupPolicyObject::GetPropertySheetPages","policy.igrouppolicyobject_getpropertysheetpages"]
old-location: policy\igrouppolicyobject_getpropertysheetpages.htm
tech.root: Policy
ms.assetid: d464d5fc-64f0-4f34-bcc0-35d92e65f79b
ms.date: 12/05/2018
ms.keywords: GetPropertySheetPages, GetPropertySheetPages method [Group Policy], GetPropertySheetPages method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetPropertySheetPages method, IGroupPolicyObject.GetPropertySheetPages, IGroupPolicyObject::GetPropertySheetPages, _win32_igrouppolicyobject_getpropertysheetpages, gpedit/IGroupPolicyObject::GetPropertySheetPages, policy.igrouppolicyobject_getpropertysheetpages
req.header: gpedit.h
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
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGroupPolicyObject::GetPropertySheetPages
 - gpedit/IGroupPolicyObject::GetPropertySheetPages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.GetPropertySheetPages
---

# IGroupPolicyObject::GetPropertySheetPages


## -description

The
    <b>GetPropertySheetPages</b> method retrieves the property sheet pages associated with the GPO.

## -parameters

### -param hPages [out]

Address of the pointer to an array of property sheet pages.

### -param uPageCount [out]

Receives the number of pages in the property sheet array.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

This method allocates memory for the array with the 
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function. When you are finished with the property sheet pages, free the array using the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>