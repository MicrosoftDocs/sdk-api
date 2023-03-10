---
UID: NN:imapi2.IDiscFormat2RawCDEventArgs
title: IDiscFormat2RawCDEventArgs (imapi2.h)
description: Use this interface to retrieve information about the current write operation. (IDiscFormat2RawCDEventArgs)
helpviewer_keywords: ["IDiscFormat2RawCDEventArgs","IDiscFormat2RawCDEventArgs interface [IMAPI]","IDiscFormat2RawCDEventArgs interface [IMAPI]","described","imapi.idiscformat2rawcdeventargs","imapi2/IDiscFormat2RawCDEventArgs"]
old-location: imapi\idiscformat2rawcdeventargs.htm
tech.root: imapi
ms.assetid: b1988883-459c-46f1-a0d1-df9500a000e1
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCDEventArgs, IDiscFormat2RawCDEventArgs interface [IMAPI], IDiscFormat2RawCDEventArgs interface [IMAPI],described, imapi.idiscformat2rawcdeventargs, imapi2/IDiscFormat2RawCDEventArgs
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
 - IDiscFormat2RawCDEventArgs
 - imapi2/IDiscFormat2RawCDEventArgs
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
 - IDiscFormat2RawCDEventArgs
---

# IDiscFormat2RawCDEventArgs interface


## -description

Use this interface to retrieve information about the current write operation. 

This interface is passed to the <a href="/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2rawcdevents-update">DDiscFormat2RawCDEvents::Update</a> method that you implement.

## -inheritance

The <b>IDiscFormat2RawCDEventArgs</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>. <b>IDiscFormat2RawCDEventArgs</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents">DDiscFormat2RawCDEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>
