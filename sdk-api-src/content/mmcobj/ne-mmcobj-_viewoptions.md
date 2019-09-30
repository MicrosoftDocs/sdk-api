---
UID: NE:mmcobj.ViewOptions
title: _ViewOptions (mmcobj.h)
author: windows-sdk-content
description: The ViewOptions enumeration is used by the Views.Add method and specifies the visibility of the view, scope tree, and toolbars, as well as the persistence state of the view.
old-location: mmc\viewoptions.htm
tech.root: mmc
ms.assetid: e3cc2834-873d-4cc1-a917-f3aeabdb2350
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVIEWOPTIONS, PPVIEWOPTIONS, PPVIEWOPTIONS enumeration pointer [MMC], PVIEWOPTIONS, PVIEWOPTIONS enumeration pointer [MMC], VIEWOPTIONS, ViewOption_Default, ViewOption_NoToolBars, ViewOption_NotPersistable, ViewOption_ScopeTreeHidden, ViewOptions, ViewOptions enumeration [MMC], _ViewOptions, _ViewOptions enumeration [MMC], _slate_viewoptions, mmc.viewoptions, mmcobj/PPVIEWOPTIONS, mmcobj/PVIEWOPTIONS, mmcobj/ViewOption_Default, mmcobj/ViewOption_NoToolBars, mmcobj/ViewOption_NotPersistable, mmcobj/ViewOption_ScopeTreeHidden, mmcobj/ViewOptions"
ms.topic: enum
f1_keywords: 
 - "mmcobj/_ViewOptions"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MmcObj.h
api_name:
 - _ViewOptions
targetos: Windows
req.typenames: "_ViewOptions, VIEWOPTIONS, *PVIEWOPTIONS"
req.redist: 
ms.custom: 19H1
---

# _ViewOptions enumeration


## -description


The 
<b>ViewOptions</b> enumeration is used by the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/views-add">Views.Add</a> method and specifies the visibility of the view, scope tree, and toolbars, as well as the persistence state of the view. These flags can be combined using a bitwise OR operation. This enumeration applies to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.


## -enum-fields




### -field ViewOption_Default

The view is added with default settings.


### -field ViewOption_ScopeTreeHidden

The view is added with the scope tree pane hidden. The user will not be able to show the scope tree, as the <b>Console Tree</b> check box will be disabled in the <b>Customize View</b> dialog box.


### -field ViewOption_NoToolBars

The view is added with toolbars hidden.


### -field ViewOption_NotPersistable

The view is added as temporary (without persistence capability).


### -field ViewOption_ActionPaneHidden




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/views-collection">Views collection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/views-add">Views.Add</a>
 

 

