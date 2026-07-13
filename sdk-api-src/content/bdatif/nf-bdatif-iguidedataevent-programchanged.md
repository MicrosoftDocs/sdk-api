---
UID: NF:bdatif.IGuideDataEvent.ProgramChanged
title: IGuideDataEvent::ProgramChanged (bdatif.h)
description: The ProgramChanged method is called when information about one or more programs has changed.
helpviewer_keywords: ["IGuideDataEvent interface [Microsoft TV Technologies]","ProgramChanged method","IGuideDataEvent.ProgramChanged","IGuideDataEvent::ProgramChanged","IGuideDataEventProgramChanged","ProgramChanged","ProgramChanged method [Microsoft TV Technologies]","ProgramChanged method [Microsoft TV Technologies]","IGuideDataEvent interface","bdatif/IGuideDataEvent::ProgramChanged","mstv.iguidedataevent_programchanged"]
old-location: mstv\iguidedataevent_programchanged.htm
tech.root: mstv
ms.assetid: 06fcf24b-5d35-4689-9c88-240fe18a46de
ms.date: 12/05/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ProgramChanged method, IGuideDataEvent.ProgramChanged, IGuideDataEvent::ProgramChanged, IGuideDataEventProgramChanged, ProgramChanged, ProgramChanged method [Microsoft TV Technologies], ProgramChanged method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ProgramChanged, mstv.iguidedataevent_programchanged
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
 - IGuideDataEvent::ProgramChanged
 - bdatif/IGuideDataEvent::ProgramChanged
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
 - IGuideDataEvent.ProgramChanged
---

# IGuideDataEvent::ProgramChanged


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ProgramChanged</b> method is called when information about one or more programs has changed.

## -parameters

### -param varProgramDescriptionID [in]

Specifies the unique identifier of the program that has changed. Call <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getprogramproperties">IGuideData::GetProgramProperties</a> to get information about the program. The value of this parameter may be an empty <b>VARIANT</b> type (VT_EMPTY); if so, examine all of the programs to determine which ones have changed.

## -returns

Return S_OK if successful, or an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent Interface</a>