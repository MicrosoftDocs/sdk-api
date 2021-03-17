---
UID: NF:mmc.IRequiredExtensions.GetFirstExtension
title: IRequiredExtensions::GetFirstExtension (mmc.h)
description: Enables the snap-in to specify the first extension snap-in its list of required extension snap-ins.
helpviewer_keywords: ["GetFirstExtension","GetFirstExtension method [MMC]","GetFirstExtension method [MMC]","IRequiredExtensions interface","IRequiredExtensions interface [MMC]","GetFirstExtension method","IRequiredExtensions.GetFirstExtension","IRequiredExtensions::GetFirstExtension","_slate_irequiredextensions_getfirstextension","mmc.irequiredextensions_getfirstextension","mmc/IRequiredExtensions::GetFirstExtension"]
old-location: mmc\irequiredextensions_getfirstextension.htm
tech.root: mmc
ms.assetid: 1c84d6ab-c855-4b89-8e36-0794e3ffdb85
ms.date: 12/05/2018
ms.keywords: GetFirstExtension, GetFirstExtension method [MMC], GetFirstExtension method [MMC],IRequiredExtensions interface, IRequiredExtensions interface [MMC],GetFirstExtension method, IRequiredExtensions.GetFirstExtension, IRequiredExtensions::GetFirstExtension, _slate_irequiredextensions_getfirstextension, mmc.irequiredextensions_getfirstextension, mmc/IRequiredExtensions::GetFirstExtension
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
 - IRequiredExtensions::GetFirstExtension
 - mmc/IRequiredExtensions::GetFirstExtension
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
 - IRequiredExtensions.GetFirstExtension
---

# IRequiredExtensions::GetFirstExtension


## -description

The <b>IRequiredExtensions::GetFirstExtension</b> method enables the snap-in to specify the first extension snap-in its list of required extension snap-ins.

## -parameters

### -param pExtCLSID [out]

A pointer to the CLSID of the first snap-in in the list of required extension snap-ins.

## -returns

This method can return one of these values.

## -remarks

MMC calls this method if 
<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-enableallextensions">IRequiredExtensions::EnableAllExtensions</a> returns a value that is not S_OK.

If this method returns S_OK, MMC adds the extension snap-in specified by pExtCLSID and then calls 
<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-getnextextension">IRequiredExtensions::GetNextExtension</a> to get the next extension snap-in in the list. If any other value is returned, MMC treats the required list as if it were empty by not adding the extension snap-in specified by pExtCLSID and not calling <b>IRequiredExtensions::GetNextExtension</b>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-irequiredextensions">IRequiredExtensions</a>



<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-enableallextensions">IRequiredExtensions::EnableAllExtensions</a>



<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-getnextextension">IRequiredExtensions::GetNextExtension</a>