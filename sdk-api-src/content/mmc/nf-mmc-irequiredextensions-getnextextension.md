---
UID: NF:mmc.IRequiredExtensions.GetNextExtension
title: IRequiredExtensions::GetNextExtension (mmc.h)
description: Enables the snap-in to specify the next extension snap-in in its list of required extension snap-ins.
helpviewer_keywords: ["GetNextExtension","GetNextExtension method [MMC]","GetNextExtension method [MMC]","IRequiredExtensions interface","IRequiredExtensions interface [MMC]","GetNextExtension method","IRequiredExtensions.GetNextExtension","IRequiredExtensions::GetNextExtension","_slate_irequiredextensions_getnextextension","mmc.irequiredextensions_getnextextension","mmc/IRequiredExtensions::GetNextExtension"]
old-location: mmc\irequiredextensions_getnextextension.htm
tech.root: mmc
ms.assetid: 09372a73-e67d-4f1f-805d-b64ca1501976
ms.date: 12/05/2018
ms.keywords: GetNextExtension, GetNextExtension method [MMC], GetNextExtension method [MMC],IRequiredExtensions interface, IRequiredExtensions interface [MMC],GetNextExtension method, IRequiredExtensions.GetNextExtension, IRequiredExtensions::GetNextExtension, _slate_irequiredextensions_getnextextension, mmc.irequiredextensions_getnextextension, mmc/IRequiredExtensions::GetNextExtension
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
 - IRequiredExtensions::GetNextExtension
 - mmc/IRequiredExtensions::GetNextExtension
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
 - IRequiredExtensions.GetNextExtension
---

# IRequiredExtensions::GetNextExtension


## -description

The <b>IRequiredExtensions::GetNextExtension</b> method enables the snap-in to specify the next extension snap-in in its list of required extension snap-ins.

## -parameters

### -param pExtCLSID [out]

A pointer to the CLSID of the next snap-in in the list of required extension snap-ins.

## -returns

This method can return one of these values.

## -remarks

MMC calls the method for the first time if 
<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-getfirstextension">IRequiredExtensions::GetFirstExtension</a> returns an S_OK value. MMC iterates the list of required extensions to add by calling <b>IRequiredExtensions::GetNextExtension</b> until it returns a value other than S_OK.

If this method returns S_OK, MMC adds the extension snap-in specified by pExtCLSID and then calls <b>IRequiredExtensions::GetNextExtension</b> again to get the next extension snap-in in the list.

If another value is returned, MMC considers the return an indicator of the end of the list. In this case, MMC does not add the extension snap-in specified by pExtCLSID and stops calling <b>IRequiredExtensions::GetNextExtension</b>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-irequiredextensions">IRequiredExtensions</a>



<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-getfirstextension">IRequiredExtensions::GetFirstExtension</a>