---
UID: NF:gpedit.IGroupPolicyObject.GetPropertySheetPages
title: IGroupPolicyObject::GetPropertySheetPages
author: windows-sdk-content
description: The GetPropertySheetPages method retrieves the property sheet pages associated with the GPO.
old-location: policy\igrouppolicyobject_getpropertysheetpages.htm
old-project: Policy
ms.assetid: d464d5fc-64f0-4f34-bcc0-35d92e65f79b
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetPropertySheetPages, GetPropertySheetPages method [Group Policy], GetPropertySheetPages method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetPropertySheetPages method, IGroupPolicyObject.GetPropertySheetPages, IGroupPolicyObject::GetPropertySheetPages, _win32_igrouppolicyobject_getpropertysheetpages, gpedit/IGroupPolicyObject::GetPropertySheetPages, policy.igrouppolicyobject_getpropertysheetpages
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpedit.dll
api_name:
-	IGroupPolicyObject.GetPropertySheetPages
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> function. When you are finished with the property sheet pages, free the array using the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>
 

 

