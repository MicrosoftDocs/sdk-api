---
UID: NF:mmcobj.SnapIns.Add
title: SnapIns::Add
author: windows-sdk-content
description: The Add method adds a snap-in to the collection. The snap-in being added must be referenced by its name, CLSID, or ProgID.
old-location: mmc\snapins_add.htm
old-project: MMC
ms.assetid: 0bc52408-21d2-40d9-9050-56398572df28
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Add, Add method [MMC], Add method [MMC],SnapIns interface, Add method [MMC],SnapIns object, SnapIns interface [MMC],Add method, SnapIns object [MMC],Add method, SnapIns.Add, SnapIns::Add, _slate_snapins.add_method, mmc.snapins_add
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
req.idl: Mmcobj.idl
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
 - Mmcndmgr.dll
api_name:
 - SnapIns.Add
 - SnapIns.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# SnapIns::Add


## -description


The 
<b>Add</b> method adds a snap-in to the collection. The snap-in being added must be referenced by its name, CLSID, or ProgID.


## -parameters




### -param SnapinNameOrCLSID

The name, CLSID, or ProgID for the registered snap-in being added to the collection.


### -param ParentSnapin

Optional 
<a href="https://msdn.microsoft.com/94a9c623-8778-4010-bb69-6ac0d7ae5ca9">SnapIn object</a> under which the new 
<b>SnapIn</b> object is added.


### -param Properties

Optional properties to be used by the snap-in. The snap-in must implement the 
<a href="https://msdn.microsoft.com/d3a7d7e0-25c3-4dfa-8984-ca9c91db8493">ISnapinProperties</a> interface for the <i>Properties</i> parameter to be useful. The <i>Properties</i> parameter can be created by the 
<a href="https://msdn.microsoft.com/b1f742b9-aae4-4d63-880c-7c3c310442f5">Document.CreateProperties</a> method.


### -param SnapIn






## -see-also




<a href="https://msdn.microsoft.com/54153853-a717-40de-a841-4532c6434c94">Application.OnSnapInAdded</a>



<a href="https://msdn.microsoft.com/b1f742b9-aae4-4d63-880c-7c3c310442f5">Document.CreateProperties</a>



<a href="https://msdn.microsoft.com/d3a7d7e0-25c3-4dfa-8984-ca9c91db8493">ISnapinProperties</a>



<a href="https://msdn.microsoft.com/a75fda6c-701f-4d68-8f91-8781fc412a0d">SnapIns.Remove</a>
 

 

