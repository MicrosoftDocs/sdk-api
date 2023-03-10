---
UID: NF:amsi.AmsiUninitialize
title: AmsiUninitialize function (amsi.h)
description: Remove the instance of the AMSI API that was originally opened by AmsiInitialize.
helpviewer_keywords: ["AmsiUninitialize","AmsiUninitialize function [Antimalware Scan Interface]","amsi.amsiuninitialize","amsi/AmsiUninitialize"]
old-location: amsi\amsiuninitialize.htm
tech.root: AMSI
ms.assetid: DAC1AAE6-3160-4A82-8E81-9CB245AFD653
ms.date: 12/05/2018
ms.keywords: AmsiUninitialize, AmsiUninitialize function [Antimalware Scan Interface], amsi.amsiuninitialize, amsi/AmsiUninitialize
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AmsiUninitialize
 - amsi/AmsiUninitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiUninitialize
---

# AmsiUninitialize function


## -description

Remove the instance of the AMSI API that was originally opened by <a href="/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>.

## -parameters

### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>.

## -see-also

<a href="/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>