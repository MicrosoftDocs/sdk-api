---
UID: NF:pla.IFolderActionCollection.Remove
title: IFolderActionCollection::Remove
author: windows-sdk-content
description: Removes a folder action from the collection based on the specified index.
old-location: pla\ifolderactioncollection_remove.htm
old-project: PLA
ms.assetid: b0894d3f-13d1-4f71-9171-592640d70969
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IFolderActionCollection interface [PLA],Remove method, IFolderActionCollection.Remove, IFolderActionCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],IFolderActionCollection interface, base.ifolderactioncollection_remove, pla.ifolderactioncollection_remove, pla/IFolderActionCollection::Remove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IFolderActionCollection.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFolderActionCollection::Remove


## -description


Removes a folder action from the collection based on the specified index.


## -parameters




### -param Index [in]

The zero-based index of the folder action to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/a3942d5f-9ec4-4461-84f9-f2fae3971e23">IFolderAction</a> interface to be removed.




## -see-also




<a href="https://msdn.microsoft.com/9b0ab26f-7e91-4d7a-9fd7-73332601dd7b">IFolderActionCollection</a>



<a href="https://msdn.microsoft.com/39597249-29d5-44a0-9954-01b9b6a62977">IFolderActionCollection::Add</a>



<a href="https://msdn.microsoft.com/357934fa-9213-466e-8104-eb9b265a98d3">IFolderActionCollection::Clear</a>
 

 

