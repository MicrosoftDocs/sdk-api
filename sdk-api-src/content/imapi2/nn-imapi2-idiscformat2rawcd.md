---
UID: NN:imapi2.IDiscFormat2RawCD
title: IDiscFormat2RawCD (imapi2.h)
description: Use this interface to write raw images to a disc device using Disc At Once (DAO) mode (also known as uninterrupted recording).
helpviewer_keywords: ["IDiscFormat2RawCD","IDiscFormat2RawCD interface [IMAPI]","IDiscFormat2RawCD interface [IMAPI]","described","imapi.idiscformat2rawcd","imapi2/IDiscFormat2RawCD"]
old-location: imapi\idiscformat2rawcd.htm
tech.root: imapi
ms.assetid: 58d9b83c-a528-4b39-b08d-a0fb8c1aece8
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD, IDiscFormat2RawCD interface [IMAPI], IDiscFormat2RawCD interface [IMAPI],described, imapi.idiscformat2rawcd, imapi2/IDiscFormat2RawCD
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
 - IDiscFormat2RawCD
 - imapi2/IDiscFormat2RawCD
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
 - IDiscFormat2RawCD
---

# IDiscFormat2RawCD interface


## -description

Use this interface to write raw images to a disc device using Disc At Once (DAO) mode (also known as uninterrupted recording). For information on DAO mode, see the latest revision of the MMC specification at ftp://ftp.t10.org/t10/drafts/mmc5.  

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2RawCD) for the class identifier and __uuidof(IDiscFormat2RawCD) for the interface identifier.

## -inheritance

The <b>IDiscFormat2RawCD</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>. <b>IDiscFormat2RawCD</b> also has these types of members:

## -remarks

To create the <b>MsftDiscFormat2RawCD</b> object in a script, use IMAPI2.MsftDiscFormat2RawCD as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="/windows/desktop/imapi/preventing-logoff-or-suspend-during-a-burn">Preventing Logoff or Suspend During a Burn</a>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>
