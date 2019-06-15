---
UID: NF:comsvcs.IComApp2Events.OnAppPaused2
title: IComApp2Events::OnAppPaused2 (comsvcs.h)
author: windows-sdk-content
description: Generated when the server application is paused or resumed to its initial state.
old-location: cos\icomapp2events_onapppaused2.htm
tech.root: cossdk
ms.assetid: 03621645-e2d1-4464-9316-7815a6e20614
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComApp2Events interface [COM+],OnAppPaused2 method, IComApp2Events.OnAppPaused2, IComApp2Events::OnAppPaused2, OnAppPaused2, OnAppPaused2 method [COM+], OnAppPaused2 method [COM+],IComApp2Events interface, _dtc_IComApp2Events_OnAppPaused2, comsvcs/IComApp2Events::OnAppPaused2, cos.icomapp2events_onapppaused2
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ComSvcs.h
api_name:
 - IComApp2Events.OnAppPaused2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComApp2Events::OnAppPaused2


## -description


Generated when the server application is paused or resumed to its initial state.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-__midl___midl_itf_autosvcs_0000_0013_0001">COMSVCSEVENTINFO</a> structure.


### -param guidApp [in]

The GUID of the application.


### -param bPaused [in]

<b>TRUE</b> if the server application is paused. <b>FALSE</b> if the application has resumed to its original state.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomapp2events">IComApp2Events</a>
 

 

