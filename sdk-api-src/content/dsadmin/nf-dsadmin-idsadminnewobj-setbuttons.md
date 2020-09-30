---
UID: NF:dsadmin.IDsAdminNewObj.SetButtons
title: IDsAdminNewObj::SetButtons (dsadmin.h)
description: The IDsAdminNewObj::SetButtons method enables or disables the &quot;Next&quot; command button in the wizard for a specific page.
helpviewer_keywords: ["IDsAdminNewObj interface [Active Directory]","SetButtons method","IDsAdminNewObj.SetButtons","IDsAdminNewObj::SetButtons","SetButtons","SetButtons method [Active Directory]","SetButtons method [Active Directory]","IDsAdminNewObj interface","_glines_idsadminnewobj_setbuttons","ad.idsadminnewobj__setbuttons","ad.idsadminnewobj_setbuttons","dsadmin/IDsAdminNewObj::SetButtons"]
old-location: ad\idsadminnewobj_setbuttons.htm
tech.root: ad
ms.assetid: 2cc888f4-b884-4e81-8dec-6f12c35d9ee4
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObj interface [Active Directory],SetButtons method, IDsAdminNewObj.SetButtons, IDsAdminNewObj::SetButtons, SetButtons, SetButtons method [Active Directory], SetButtons method [Active Directory],IDsAdminNewObj interface, _glines_idsadminnewobj_setbuttons, ad.idsadminnewobj__setbuttons, ad.idsadminnewobj_setbuttons, dsadmin/IDsAdminNewObj::SetButtons
req.header: dsadmin.h
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
req.dll: DSAdmin.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsAdminNewObj::SetButtons
 - dsadmin/IDsAdminNewObj::SetButtons
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNewObj.SetButtons
---

# IDsAdminNewObj::SetButtons


## -description

The <b>IDsAdminNewObj::SetButtons</b> method enables or disables the "Next" command button in the wizard for a specific page.

## -parameters

### -param nCurrIndex [in]

Contains the zero-based index of the wizard page for which the "Next" button will be enabled or disabled. This index is relative to the page count of the wizard extension that calls the method.

### -param bValid [in]

Specifies if the "Next" command button is enabled or disabled. If this value is zero, the "Next" command button is disabled. If this value is nonzero, the "Next" command button is enabled.

## -returns

This method can return one of these values.


Returns one of the following values.

## -remarks

No assumption should be made regarding the state of the "Next" command button when the page is first displayed. The object creation extension should set the state of the "Next" command button when the page is first displayed and when the data in the page changes. If the data in the page is not mandatory, then the "Next" button should be enabled when the page is first displayed and the state should not be changed by the extension.

If the extension calling the function is a primary extension with a single page and there are no secondary extensions loaded, for example: the wizard has a single page, the command buttons are; "OK" and "Cancel", instead of "Back", "Next", and "Cancel". In this case, a call to this function will enable or disable the "OK" button.

## -see-also

<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a>