---
UID: NF:mmc.IRequiredExtensions.EnableAllExtensions
title: IRequiredExtensions::EnableAllExtensions (mmc.h)
description: The IRequiredExtensions::EnableAllExtensions method enables the snap-in to specify that all extension snap-ins registered for the snap-in are required.
helpviewer_keywords: ["EnableAllExtensions","EnableAllExtensions method [MMC]","EnableAllExtensions method [MMC]","IRequiredExtensions interface","IRequiredExtensions interface [MMC]","EnableAllExtensions method","IRequiredExtensions.EnableAllExtensions","IRequiredExtensions::EnableAllExtensions","_slate_irequiredextensions_enableallextensions","mmc.irequiredextensions_enableallextensions","mmc/IRequiredExtensions::EnableAllExtensions"]
old-location: mmc\irequiredextensions_enableallextensions.htm
tech.root: mmc
ms.assetid: f7278976-8f15-43a4-b9ef-fb1952fdd455
ms.date: 12/05/2018
ms.keywords: EnableAllExtensions, EnableAllExtensions method [MMC], EnableAllExtensions method [MMC],IRequiredExtensions interface, IRequiredExtensions interface [MMC],EnableAllExtensions method, IRequiredExtensions.EnableAllExtensions, IRequiredExtensions::EnableAllExtensions, _slate_irequiredextensions_enableallextensions, mmc.irequiredextensions_enableallextensions, mmc/IRequiredExtensions::EnableAllExtensions
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRequiredExtensions::EnableAllExtensions
 - mmc/IRequiredExtensions::EnableAllExtensions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IRequiredExtensions.EnableAllExtensions
---

# IRequiredExtensions::EnableAllExtensions


## -description

The <b>IRequiredExtensions::EnableAllExtensions</b> method enables the snap-in to specify that all extension snap-ins registered for the snap-in are required.



## -returns

This method can return one of these values.

## -remarks

If this method returns S_OK, MMC adds all registered extensions. If any other value is returned, MMC calls 
<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-getfirstextension">IRequiredExtensions::GetFirstExtension</a> to attempt to add the first required extension of the snap-in's list of required extensions.

If one of the required extensions can't be loaded, MMC skips it and continues to query the snap-in for the rest of them. There is no indication back to the snap-in when an extension fails to load.

If all extensions are requested, they are loaded in the order in which they are found in the registry. First, all the registered node types for the snap-in are read. Then, for each node type, all the extensions are read in the following order: namespace, context menu, toolbar, property sheet, taskpad.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-irequiredextensions">IRequiredExtensions</a>



<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-getfirstextension">IRequiredExtensions::GetFirstExtension</a>
