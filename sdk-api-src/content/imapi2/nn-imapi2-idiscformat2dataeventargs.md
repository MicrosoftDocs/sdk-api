---
UID: NN:imapi2.IDiscFormat2DataEventArgs
title: IDiscFormat2DataEventArgs (imapi2.h)
description: Use this interface to retrieve information about the current write operation. (IDiscFormat2DataEventArgs)
helpviewer_keywords: ["IDiscFormat2DataEventArgs","IDiscFormat2DataEventArgs interface [IMAPI]","IDiscFormat2DataEventArgs interface [IMAPI]","described","imapi.idiscformat2dataeventargs","imapi2/IDiscFormat2DataEventArgs"]
old-location: imapi\idiscformat2dataeventargs.htm
tech.root: imapi
ms.assetid: 6bf149d3-62ea-4ef5-8d45-44df9ad4982c
ms.date: 12/05/2018
ms.keywords: IDiscFormat2DataEventArgs, IDiscFormat2DataEventArgs interface [IMAPI], IDiscFormat2DataEventArgs interface [IMAPI],described, imapi.idiscformat2dataeventargs, imapi2/IDiscFormat2DataEventArgs
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
 - IDiscFormat2DataEventArgs
 - imapi2/IDiscFormat2DataEventArgs
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
 - IDiscFormat2DataEventArgs
---

# IDiscFormat2DataEventArgs interface


## -description

Use this interface to retrieve information about the current write operation. 

This interface is passed to the <a href="/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2dataevents-update">DDiscFormat2DataEvents::Update</a> method that you implement.

## -inheritance

The <b>IDiscFormat2DataEventArgs</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>. <b>IDiscFormat2DataEventArgs</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents">DDiscFormat2DataEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>
