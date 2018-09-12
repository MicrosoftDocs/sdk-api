---
UID: NF:bdatif.IGuideDataEvent.ProgramChanged
title: IGuideDataEvent::ProgramChanged
author: windows-sdk-content
description: The ProgramChanged method is called when information about one or more programs has changed.
old-location: mstv\iguidedataevent_programchanged.htm
tech.root: mstv
ms.assetid: 06fcf24b-5d35-4689-9c88-240fe18a46de
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ProgramChanged method, IGuideDataEvent.ProgramChanged, IGuideDataEvent::ProgramChanged, IGuideDataEventProgramChanged, ProgramChanged, ProgramChanged method [Microsoft TV Technologies], ProgramChanged method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ProgramChanged, mstv.iguidedataevent_programchanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideDataEvent.ProgramChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideDataEvent::ProgramChanged


## -description



The <b>ProgramChanged</b> method is called when information about one or more programs has changed.




## -parameters




### -param varProgramDescriptionID [in]

Specifies the unique identifier of the program that has changed. Call <a href="https://msdn.microsoft.com/57eb55bf-49d9-471e-b59c-0d87aa3c3e3c">IGuideData::GetProgramProperties</a> to get information about the program. The value of this parameter may be an empty <b>VARIANT</b> type (VT_EMPTY); if so, examine all of the programs to determine which ones have changed.


## -returns



Return S_OK if successful, or an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9da565f2-fbcb-4d71-ae40-7d9821f46630">IGuideDataEvent Interface</a>
 

 

