---
UID: NF:dsadmin.IDsAdminNewObj.SetButtons
title: IDsAdminNewObj::SetButtons
author: windows-sdk-content
description: The IDsAdminNewObj::SetButtons method enables or disables the &#0034;Next&#0034; command button in the wizard for a specific page.
old-location: ad\idsadminnewobj_setbuttons.htm
old-project: AD
ms.assetid: 2cc888f4-b884-4e81-8dec-6f12c35d9ee4
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDsAdminNewObj interface [Active Directory],SetButtons method, IDsAdminNewObj.SetButtons, IDsAdminNewObj::SetButtons, SetButtons, SetButtons method [Active Directory], SetButtons method [Active Directory],IDsAdminNewObj interface, _glines_idsadminnewobj_setbuttons, ad.idsadminnewobj__setbuttons, ad.idsadminnewobj_setbuttons, dsadmin/IDsAdminNewObj::SetButtons
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DRT_ADDRESS_LIST, *PDRT_ADDRESS_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DSAdmin.dll
api_name:
-	IDsAdminNewObj.SetButtons
product: Windows
targetos: Windows
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
---

# IDsAdminNewObj::SetButtons


## -description


The <b>IDsAdminNewObj::SetButtons</b> method enables or disables the "Next" command button in the wizard for a specific page.


## -parameters




### -param nCurrIndex




### -param bValid [in]

Specifies if the "Next" command button is enabled or disabled. If this value is zero, the "Next" command button is disabled. If this value is nonzero, the "Next" command button is enabled.


#### - nCurrentIndex [in]

Contains the zero-based index of the wizard page for which the "Next" button will be enabled or disabled. This index is relative to the page count of the wizard extension that calls the method.


## -returns



This method can return one of these values.


Returns one of the following values.






## -remarks



No assumption should be made regarding the state of the "Next" command button when the page is first displayed. The object creation extension should set the state of the "Next" command button when the page is first displayed and when the data in the page changes. If the data in the page is not mandatory, then the "Next" button should be enabled when the page is first displayed and the state should not be changed by the extension.

If the extension calling the function is a primary extension with a single page and there are no secondary extensions loaded, for example: the wizard has a single page, the command buttons are; "OK" and "Cancel", instead of "Back", "Next", and "Cancel". In this case, a call to this function will enable or disable the "OK" button.




## -see-also




<a href="https://msdn.microsoft.com/b38016a2-bbb7-4715-81cc-bd9911fb5a3b">IDsAdminNewObj</a>
 

 

