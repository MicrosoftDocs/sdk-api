---
UID: NF:mmc.IRequiredExtensions.EnableAllExtensions
title: IRequiredExtensions::EnableAllExtensions
author: windows-sdk-content
description: The IRequiredExtensions::EnableAllExtensions method enables the snap-in to specify that all extension snap-ins registered for the snap-in are required.
old-location: mmc\irequiredextensions_enableallextensions.htm
tech.root: mmc
ms.assetid: f7278976-8f15-43a4-b9ef-fb1952fdd455
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: EnableAllExtensions, EnableAllExtensions method [MMC], EnableAllExtensions method [MMC],IRequiredExtensions interface, IRequiredExtensions interface [MMC],EnableAllExtensions method, IRequiredExtensions.EnableAllExtensions, IRequiredExtensions::EnableAllExtensions, _slate_irequiredextensions_enableallextensions, mmc.irequiredextensions_enableallextensions, mmc/IRequiredExtensions::EnableAllExtensions
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Mmc.h
api_name:
 - IRequiredExtensions.EnableAllExtensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmc.h
: 
- IRequiredExtensions.EnableAllExtensions
: 
---

# IRequiredExtensions::EnableAllExtensions


## -description


The <b>IRequiredExtensions::EnableAllExtensions</b> method enables the snap-in to specify that all extension snap-ins registered for the snap-in are required.


## -parameters






## -returns



This method can return one of these values.




## -remarks



If this method returns S_OK, MMC adds all registered extensions. If any other value is returned, MMC calls 
<a href="https://msdn.microsoft.com/1c84d6ab-c855-4b89-8e36-0794e3ffdb85">IRequiredExtensions::GetFirstExtension</a> to attempt to add the first required extension of the snap-in's list of required extensions.

If one of the required extensions can't be loaded, MMC skips it and continues to query the snap-in for the rest of them. There is no indication back to the snap-in when an extension fails to load.

If all extensions are requested, they are loaded in the order in which they are found in the registry. First, all the registered node types for the snap-in are read. Then, for each node type, all the extensions are read in the following order: namespace, context menu, toolbar, property sheet, taskpad.




## -see-also




<a href="https://msdn.microsoft.com/55832db9-30d9-4a5f-bfef-a014b1050f22">IRequiredExtensions</a>



<a href="https://msdn.microsoft.com/1c84d6ab-c855-4b89-8e36-0794e3ffdb85">IRequiredExtensions::GetFirstExtension</a>
 

 

