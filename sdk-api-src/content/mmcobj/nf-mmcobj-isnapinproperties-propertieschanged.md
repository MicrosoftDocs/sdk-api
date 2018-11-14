---
UID: NF:mmcobj.ISnapinProperties.PropertiesChanged
title: ISnapinProperties::PropertiesChanged
author: windows-sdk-content
description: Called when a property is added, changed, or deleted.
old-location: mmc\isnapinproperties_propertieschanged.htm
tech.root: mmc
ms.assetid: 6e64a620-9c1d-4803-81a0-ec432c30fbc9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ISnapinProperties interface [MMC],PropertiesChanged method, ISnapinProperties.PropertiesChanged, ISnapinProperties::PropertiesChanged, PropertiesChanged, PropertiesChanged method [MMC], PropertiesChanged method [MMC],ISnapinProperties interface, _slate_isnapinproperties_propertieschanged, mmc.isnapinproperties_propertieschanged, mmcobj/ISnapinProperties::PropertiesChanged
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: 
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
 - COM
api_location:
 - Mmcobj.h
api_name:
 - ISnapinProperties.PropertiesChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmcobj.h
: 
- ISnapinProperties.PropertiesChanged
: 
---

# ISnapinProperties::PropertiesChanged


## -description


The 
<b>PropertiesChanged</b> method is called when a property is added, changed, or deleted. A snap-in can reject the change or deletion by returning E_FAIL.


## -parameters




### -param cProperties [in]

The number of 
<a href="https://msdn.microsoft.com/0815d6a0-ddc2-43d1-aafd-5a05352557fc">MMC_SNAPIN_PROPERTY</a> structures provided by <i>pProperties</i>.


### -param pProperties [in]

An array of 
<a href="https://msdn.microsoft.com/0815d6a0-ddc2-43d1-aafd-5a05352557fc">MMC_SNAPIN_PROPERTY</a> structures.


## -returns



If successful, the return value is <b>S_OK</b>; a snap-in can prevent a change or deletion from occurring by returning <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/c380d562-0acb-4c90-9460-6007a8eeb596">MMC_PROPERTY_ACTION</a>



<a href="https://msdn.microsoft.com/0815d6a0-ddc2-43d1-aafd-5a05352557fc">MMC_SNAPIN_PROPERTY</a>
 

 

