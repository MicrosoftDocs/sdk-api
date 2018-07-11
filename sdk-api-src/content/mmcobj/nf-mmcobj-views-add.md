---
UID: NF:mmcobj.Views.Add
title: Views::Add
author: windows-sdk-content
description: The Add method adds a view at a specified root node.
old-location: mmc\views_add.htm
old-project: mmc
ms.assetid: 86c809b4-6533-4e02-a49e-f141fac228b1
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: Add, Add method [MMC], Add method [MMC],Views interface, Add method [MMC],Views object, ViewOption_Default, ViewOption_NoToolBars, ViewOption_NotPersistable, ViewOption_ScopeTreeHidden, Views interface [MMC],Add method, Views object [MMC],Add method, Views.Add, Views::Add, _slate_views.add_method, mmc.views_add
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
 - Views.Add
 - Views.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# Views::Add


## -description


The 
<b>Add</b> method adds a view at a specified root node.


## -parameters




### -param Node

The node to serve as the root of the added view.


### -param viewOptions






#### - ViewOptions

This parameter can be one or more of the following 
<a href="https://msdn.microsoft.com/e3cc2834-873d-4cc1-a917-f3aeabdb2350">ViewOptions</a> enumeration types. These flags can be combined using a bitwise OR operation.



#### ViewOption_Default

The view is added with default settings.



#### ViewOption_ScopeTreeHidden

The view is added with the scope tree pane hidden. The user will not be able to show the scope tree, as the <i>Console Tree</i> check box will be disabled in the <i>Customize View</i> dialog.



#### ViewOption_NoToolBars

The view is added with toolbars hidden.



#### ViewOption_NotPersistable

The view is temporary (without persistence capability).


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e3cc2834-873d-4cc1-a917-f3aeabdb2350">ViewOptions</a>



<a href="https://msdn.microsoft.com/92dac3b7-c766-4d7e-8835-427b026f5c60">Views.Count</a>



<a href="https://msdn.microsoft.com/adf1d8e4-96cd-4af0-bbd2-ec162ca382ad">Views.Item</a>
 

 

