---
UID: NF:tuner.IEnumTuningSpaces.Next
title: IEnumTuningSpaces::Next
author: windows-sdk-content
description: The Next method retrieves the next n elements in the collection.
old-location: mstv\ienumtuningspaces_next.htm
tech.root: mstv
ms.assetid: 1220d006-10e9-4e64-8a18-8828b62d5da9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumTuningSpaces interface [Microsoft TV Technologies],Next method, IEnumTuningSpaces.Next, IEnumTuningSpaces::Next, IEnumTuningSpacesNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumTuningSpaces interface, mstv.ienumtuningspaces_next, tuner/IEnumTuningSpaces::Next
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IEnumTuningSpaces.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumTuningSpaces::Next


## -description



The <b>Next</b> method retrieves the next n elements in the collection.




## -parameters




### -param celt [in]

The number of elements to retrieve.


### -param rgelt [out]

Address of an array of <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface pointers that will receive the retrieved Tuning Space objects.


### -param pceltFetched [out]

Receives the number of elements actually retrieved.


## -returns



Returns S_OK if successful. This method will succeed even if <i>celt</i> is zero. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/9b64a48f-ebab-46af-a89d-b8bc488d85da">IEnumTuningSpaces Interface</a>
 

 

