---
UID: NN:imapi2.IDiscFormat2TrackAtOnce
title: IDiscFormat2TrackAtOnce (imapi2.h)
description: Use this interface to write audio to blank CD-R or CD-RW media in Track-At-Once mode.
helpviewer_keywords: ["IDiscFormat2TrackAtOnce","IDiscFormat2TrackAtOnce interface [IMAPI]","IDiscFormat2TrackAtOnce interface [IMAPI]","described","imapi.idiscformat2trackatonce","imapi2/IDiscFormat2TrackAtOnce"]
old-location: imapi\idiscformat2trackatonce.htm
tech.root: imapi
ms.assetid: 27f2d248-1c83-4784-82f9-75ce0a038b87
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce, IDiscFormat2TrackAtOnce interface [IMAPI], IDiscFormat2TrackAtOnce interface [IMAPI],described, imapi.idiscformat2trackatonce, imapi2/IDiscFormat2TrackAtOnce
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
 - IDiscFormat2TrackAtOnce
 - imapi2/IDiscFormat2TrackAtOnce
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
 - IDiscFormat2TrackAtOnce
---

# IDiscFormat2TrackAtOnce interface


## -description

Use this interface to write audio to blank CD-R or CD-RW media in Track-At-Once mode.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2TrackAtOnce) for the class identifier and __uuidof(IDiscFormat2TrackAtOnce) for the interface identifier.

## -inheritance

The <b>IDiscFormat2TrackAtOnce</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>. <b>IDiscFormat2TrackAtOnce</b> also has these types of members:

## -remarks

To create the <b>MsftDiscFormat2TrackAtOnce</b> object in a script, use IMAPI2.MsftDiscFormat2TrackAtOnce as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="/windows/desktop/imapi/preventing-logoff-or-suspend-during-a-burn">Preventing Logoff or Suspend During a Burn</a>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>
