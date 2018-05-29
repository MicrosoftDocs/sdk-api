---
UID: NF:ocidl.IPropertyPage.Show
title: IPropertyPage::Show
author: windows-sdk-content
description: Makes the property page dialog box visible or invisible. If the page is made visible, the page should set the focus to itself, specifically to the first property on the page.
old-location: com\ipropertypage_show.htm
old-project: com
ms.assetid: f89aa820-a3d3-4a41-b2b2-9ee48354fbeb
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IPropertyPage interface [COM],Show method, IPropertyPage.Show, IPropertyPage::Show, Show, Show method [COM], Show method [COM],IPropertyPage interface, _ctrl_ipropertypage_show, com.ipropertypage_show, ocidl/IPropertyPage::Show
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPropertyPage.Show
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPropertyPage::Show


## -description


Makes the property page dialog box visible or invisible. If the page is made visible, the page should set the focus to itself, specifically to the first property on the page.


## -parameters




### -param nCmdShow [in]

A command describing whether to become visible (SW_SHOW or SW_SHOWNORMAL) or hidden (SW_HIDE). No other values are valid for this parameter.


## -returns



This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, and S_OK.




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calls to this method must occur after a call to <a href="https://msdn.microsoft.com/4756d06d-0ffc-4214-9c2b-d9cb169b4337">IPropertyPage::Activate</a> and before a corresponding call to <a href="https://msdn.microsoft.com/545f7c3d-3c6f-42c2-b472-3da3bc184200">IPropertyPage::Deactivate</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not a valid return value. E_OUTOFMEMORY is not a valid return value, since no memory should be used in implementing this method.




## -see-also




<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>
 

 

