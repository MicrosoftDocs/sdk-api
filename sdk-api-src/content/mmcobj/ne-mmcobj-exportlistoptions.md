---
UID: NE:mmcobj.ExportListOptions
title: ExportListOptions
author: windows-sdk-content
description: The ExportListOptions enumeration is used by the View.ExportList method and specifies options when writing list view contents to a file.
old-location: mmc\exportlistoptions.htm
old-project: MMC
ms.assetid: cfdb5648-8573-4c5a-85c2-7a5d3d63a5f3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: EXPORTLISTOPTIONS, ExportListOptions, ExportListOptions enumeration [MMC], ExportListOptions_Default, ExportListOptions_SelectedItemsOnly, ExportListOptions_TabDelimited, ExportListOptions_Unicode, _ExportListOptions, _ExportListOptions enumeration [MMC], _slate_exportlistoptions, mmc.exportlistoptions, mmcobj/ExportListOptions, mmcobj/ExportListOptions_Default, mmcobj/ExportListOptions_SelectedItemsOnly, mmcobj/ExportListOptions_TabDelimited, mmcobj/ExportListOptions_Unicode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MmcObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "_ExportListOptions, EXPORTLISTOPTIONS"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MmcObj.h
api_name:
 - _ExportListOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ExportListOptions enumeration


## -description


The 
<b>ExportListOptions</b> enumeration is used by the 
<a href="https://msdn.microsoft.com/ff552b80-2f5f-4425-9157-71f7c7fb5a44">View.ExportList</a> method and specifies options when writing list view contents to a file. These values can be combined using a bitwise OR operation. This enumeration applies to the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation Object Model</a>.


## -enum-fields




### -field ExportListOptions_Default

Default list export option. If this is the only flag specified in the call to <a href="https://msdn.microsoft.com/ff552b80-2f5f-4425-9157-71f7c7fb5a44">View.ExportList</a>, then the list view contents are exported as comma-delimited ANSI text.


### -field ExportListOptions_Unicode

The list is exported as Unicode text.


### -field ExportListOptions_TabDelimited

The list is exported as tab-delimited text.


### -field ExportListOptions_SelectedItemsOnly

The exported list contains only currently selected items.


## -see-also




<a href="https://msdn.microsoft.com/004043d1-c7c3-4385-a4f5-a7fbf616d05c">View object</a>



<a href="https://msdn.microsoft.com/ff552b80-2f5f-4425-9157-71f7c7fb5a44">View.ExportList</a>
 

 

