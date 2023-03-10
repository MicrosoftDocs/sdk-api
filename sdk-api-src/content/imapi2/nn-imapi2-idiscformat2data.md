---
UID: NN:imapi2.IDiscFormat2Data
title: IDiscFormat2Data (imapi2.h)
description: Use this interface to write a data stream to a disc.
helpviewer_keywords: ["IDiscFormat2Data","IDiscFormat2Data interface [IMAPI]","IDiscFormat2Data interface [IMAPI]","described","imapi.idiscformat2data","imapi2/IDiscFormat2Data"]
old-location: imapi\idiscformat2data.htm
tech.root: imapi
ms.assetid: 6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data, IDiscFormat2Data interface [IMAPI], IDiscFormat2Data interface [IMAPI],described, imapi.idiscformat2data, imapi2/IDiscFormat2Data
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
 - IDiscFormat2Data
 - imapi2/IDiscFormat2Data
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
 - IDiscFormat2Data
---

# IDiscFormat2Data interface


## -description

Use this interface to write a data stream to a disc.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2Data) for the class identifier and __uuidof(IDiscFormat2Data) for the interface identifier.

## -inheritance

The <b>IDiscFormat2Data</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>. <b>IDiscFormat2Data</b> also has these types of members:

## -remarks

To create the <b>MsftDiscFormat2Data</b> object in a script, use IMAPI2.MsftDiscFormat2Data as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="/windows/desktop/imapi/preventing-logoff-or-suspend-during-a-burn">Preventing Logoff or Suspend During a Burn</a>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>
