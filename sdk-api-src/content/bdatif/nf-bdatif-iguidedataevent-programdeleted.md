---
UID: NF:bdatif.IGuideDataEvent.ProgramDeleted
title: IGuideDataEvent::ProgramDeleted (bdatif.h)
description: The ProgramDeleted method is called when a program has been deleted.
helpviewer_keywords: ["IGuideDataEvent interface [Microsoft TV Technologies]","ProgramDeleted method","IGuideDataEvent.ProgramDeleted","IGuideDataEvent::ProgramDeleted","IGuideDataEventProgramDeleted","ProgramDeleted","ProgramDeleted method [Microsoft TV Technologies]","ProgramDeleted method [Microsoft TV Technologies]","IGuideDataEvent interface","bdatif/IGuideDataEvent::ProgramDeleted","mstv.iguidedataevent_programdeleted"]
old-location: mstv\iguidedataevent_programdeleted.htm
tech.root: mstv
ms.assetid: 4a71e139-1c09-473c-8195-0a55601d2f17
ms.date: 12/05/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ProgramDeleted method, IGuideDataEvent.ProgramDeleted, IGuideDataEvent::ProgramDeleted, IGuideDataEventProgramDeleted, ProgramDeleted, ProgramDeleted method [Microsoft TV Technologies], ProgramDeleted method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ProgramDeleted, mstv.iguidedataevent_programdeleted
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IGuideDataEvent::ProgramDeleted
 - bdatif/IGuideDataEvent::ProgramDeleted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideDataEvent.ProgramDeleted
---

# IGuideDataEvent::ProgramDeleted


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ProgramDeleted</b> method is called when a program has been deleted.



Currently the <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> (TIF) does not support this event, so this method is not called.

## -parameters

### -param varProgramDescriptionID [in]

Specifies the unique identifier of the program that was deleted.

## -returns

Return S_OK if successful, or an error code.

## -remarks

The event sink is not required to support this event; it may return E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent Interface</a>