---
UID: NF:tuner.IESEventServiceConfiguration.SetParent
title: IESEventServiceConfiguration::SetParent
author: windows-sdk-content
description: Sets a parent event service for an event service that implements the IESEventService interface. Once an event service has set a parent, it can receive advise events from the parent.
old-location: mstv\ieseventserviceconfiguration_setparent.htm
tech.root: MSTV
ms.assetid: cfb931e9-f20f-4812-9d6b-cf8b651b7e7a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],SetParent method, IESEventServiceConfiguration.SetParent, IESEventServiceConfiguration::SetParent, SetParent, SetParent method [Microsoft TV Technologies], SetParent method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_setparent, tuner/IESEventServiceConfiguration::SetParent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IESEventServiceConfiguration.SetParent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- IESEventServiceConfiguration.SetParent
: 
---

# IESEventServiceConfiguration::SetParent


## -description


Sets a parent event service for an event service that implements the <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> interface. Once an event service has set a parent, it can receive advise events from the parent.


## -parameters




### -param pEventService [in]

Pointer to the <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> interface for the parent event service.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a>



<a href="https://msdn.microsoft.com/0b901732-42e1-4f50-904c-75d8202bb5b7">IESEventServiceConfiguration</a>
 

 

