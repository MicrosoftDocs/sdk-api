---
UID: NF:mmc.IExtendPropertySheet.QueryPagesFor
title: IExtendPropertySheet::QueryPagesFor
author: windows-sdk-content
description: Determines whether the object requires pages.
old-location: mmc\iextendpropertysheet_querypagesfor.htm
old-project: MMC
ms.assetid: F21A0AA2-8F79-4AEA-A5B1-8D650BE14C9F
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: IExtendPropertySheet interface [MMC],QueryPagesFor method, IExtendPropertySheet.QueryPagesFor, IExtendPropertySheet::QueryPagesFor, QueryPagesFor, QueryPagesFor method [MMC], QueryPagesFor method [MMC],IExtendPropertySheet interface, mmc.iextendpropertysheet_querypagesfor, mmc/IExtendPropertySheet::QueryPagesFor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendPropertySheet.QueryPagesFor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IExtendPropertySheet::QueryPagesFor


## -description


Determines whether the object requires pages.


## -parameters




### -param lpDataObject [in]

A pointer to the 
<a href="_ole_idataobject">IDataObject</a> interface on the object that contains context information about the scope or result item.


## -returns



This method can return one of these values.




## -remarks



The console calls this method to determine whether the 
<b>Properties</b> menu item should be added to the context menu.




## -see-also




<a href="https://msdn.microsoft.com/b41508bf-8399-44bb-abad-754aa5d32776">Adding Property Pages and Wizard Pages</a>



<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/c3c75e69-e16c-425b-bd8c-3c6f2e5ce2db">IExtendPropertySheet</a>



<a href="https://msdn.microsoft.com/e2115929-692e-4e59-bcdb-f37b02c53224">IPropertySheetCallback</a>
 

 

