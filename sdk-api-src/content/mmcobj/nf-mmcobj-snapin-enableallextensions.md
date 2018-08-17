---
UID: NF:mmcobj.SnapIn.EnableAllExtensions
title: SnapIn::EnableAllExtensions
author: windows-sdk-content
description: The EnableAllExtensions method determines whether or not all extensions for the snap-in are enabled. This method is the programmatic equivalent of the &#0034;Add all extensions&#0034; check box in the Snap-In Manager.
old-location: mmc\snapin_enableallextensions.htm
old-project: mmc
ms.assetid: 9aee0bb9-ad2c-4bd5-97be-e38cc2425d70
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: EnableAllExtensions, EnableAllExtensions method [MMC], EnableAllExtensions method [MMC],SnapIn interface, EnableAllExtensions method [MMC],SnapIn object, SnapIn interface [MMC],EnableAllExtensions method, SnapIn object [MMC],EnableAllExtensions method, SnapIn.EnableAllExtensions, SnapIn::EnableAllExtensions, _slate_snapin.enableallextensions_method, mmc.snapin_enableallextensions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmcobj.h
req.include-header: 
req.redist: 
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
 - Mmcndmgr.dll
api_name:
 - SnapIn.EnableAllExtensions
 - SnapIn.EnableAllExtensions
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# SnapIn::EnableAllExtensions


## -description


The 
<b>EnableAllExtensions</b> method determines whether or not all extensions for the snap-in are enabled. This method is the programmatic equivalent of the "Add all extensions" check box in the Snap-In Manager.


## -parameters




### -param Enable

Value that determines whether all extensions are enabled. To add all available extensions, set <i>Enable</i> to 1. To add or exclude individual extensions, call this method with <i>Enable</i> set to 0 and then call 
<a href="https://msdn.microsoft.com/7e060b12-880d-4639-8571-63e237446847">Extension.Enable</a> to enable or disable individual extension snap-ins.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/ac49922e-5e13-4936-8f57-8901e4837fe3">Extensions collection</a>



<a href="https://msdn.microsoft.com/d7504a23-937e-4180-9c63-62601791529c">SnapIn.Extensions</a>
 

 

