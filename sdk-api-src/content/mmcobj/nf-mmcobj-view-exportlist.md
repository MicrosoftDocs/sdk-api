---
UID: NF:mmcobj.View.ExportList
title: View::ExportList
author: windows-sdk-content
description: The ExportList method exports the selected list to the specified file.
old-location: mmc\view_exportlist.htm
old-project: MMC
ms.assetid: ff552b80-2f5f-4425-9157-71f7c7fb5a44
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ExportList, ExportList method [MMC], ExportList method [MMC],View interface, ExportList method [MMC],View object, ExportListOptions_Default, ExportListOptions_SelectedItemsOnly, ExportListOptions_TabDelimited, ExportListOptions_Unicode, View interface [MMC],ExportList method, View object [MMC],ExportList method, View.ExportList, View::ExportList, _slate_view.exportlist_method, mmc.view_exportlist
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MMCObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_PROPERTY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.exe
api_name:
 - View.ExportList
 - View.ExportList
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# View::ExportList


## -description


The 
<b>ExportList</b> method exports the selected list to the specified file.


## -parameters




### -param File

The name of the export file.


### -param exportoptions

This parameter can be one or more of the following 
<a href="https://msdn.microsoft.com/cfdb5648-8573-4c5a-85c2-7a5d3d63a5f3">ExportListOptions</a> values. These flags can be combined using a bitwise OR operation.



#### ExportListOptions_Default

Default list export option. If this is the only flag specified in the call to <b>View.ExportList</b>, then the list view contents are exported as comma-delimited ANSI text.



#### ExportListOptions_Unicode

The list is exported as Unicode text.



#### ExportListOptions_TabDelimited

The list is exported as tab-delimited text.



#### ExportListOptions_SelectedItemsOnly

The exported list contains only selected items.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/cfdb5648-8573-4c5a-85c2-7a5d3d63a5f3">ExportListOptions</a>
 

 

