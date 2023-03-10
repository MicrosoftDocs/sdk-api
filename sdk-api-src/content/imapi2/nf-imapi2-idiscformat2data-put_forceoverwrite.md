---
UID: NF:imapi2.IDiscFormat2Data.put_ForceOverwrite
title: IDiscFormat2Data::put_ForceOverwrite (imapi2.h)
description: Determines if the data writer must overwrite the disc on overwritable media types. (Put)
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","put_ForceOverwrite method","IDiscFormat2Data.put_ForceOverwrite","IDiscFormat2Data::put_ForceOverwrite","imapi.idiscformat2data_put_forceoverwrite","imapi2/IDiscFormat2Data::put_ForceOverwrite","put_ForceOverwrite","put_ForceOverwrite method [IMAPI]","put_ForceOverwrite method [IMAPI]","IDiscFormat2Data interface"]
old-location: imapi\idiscformat2data_put_forceoverwrite.htm
tech.root: imapi
ms.assetid: 19b77c94-ad2a-42c8-8042-267a48036dac
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],put_ForceOverwrite method, IDiscFormat2Data.put_ForceOverwrite, IDiscFormat2Data::put_ForceOverwrite, imapi.idiscformat2data_put_forceoverwrite, imapi2/IDiscFormat2Data::put_ForceOverwrite, put_ForceOverwrite, put_ForceOverwrite method [IMAPI], put_ForceOverwrite method [IMAPI],IDiscFormat2Data interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IDiscFormat2Data::put_ForceOverwrite
 - imapi2/IDiscFormat2Data::put_ForceOverwrite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Data.put_ForceOverwrite
---

# IDiscFormat2Data::put_ForceOverwrite


## -description

Determines if the data writer must overwrite the disc on overwritable media types.

## -parameters

### -param value [in]

Is VARIANT_TRUE if the data writer must overwrite the disc on overwritable media types; otherwise, VARIANT_FALSE. The default is VARIANT_FALSE.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>
