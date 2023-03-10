---
UID: NF:manipulations.IManipulationProcessor.GetAngularVelocity
title: IManipulationProcessor::GetAngularVelocity (manipulations.h)
description: The GetAngularVelocity method calculates the rotational velocity that the target object is moving at.
helpviewer_keywords: ["GetAngularVelocity","GetAngularVelocity method [Windows Touch]","GetAngularVelocity method [Windows Touch]","IManipulationProcessor interface","IManipulationProcessor interface [Windows Touch]","GetAngularVelocity method","IManipulationProcessor.GetAngularVelocity","IManipulationProcessor::GetAngularVelocity","manipulations/IManipulationProcessor::GetAngularVelocity","wintouch.imanipulationprocessor_getangularvelocity"]
old-location: wintouch\imanipulationprocessor_getangularvelocity.htm
tech.root: wintouch
ms.assetid: 3253837f-c5ea-47f7-ba0a-86e0ed4e228e
ms.date: 12/05/2018
ms.keywords: GetAngularVelocity, GetAngularVelocity method [Windows Touch], GetAngularVelocity method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetAngularVelocity method, IManipulationProcessor.GetAngularVelocity, IManipulationProcessor::GetAngularVelocity, manipulations/IManipulationProcessor::GetAngularVelocity, wintouch.imanipulationprocessor_getangularvelocity
req.header: manipulations.h
req.include-header: Manipulations_i.c
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IManipulationProcessor::GetAngularVelocity
 - manipulations/IManipulationProcessor::GetAngularVelocity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IManipulationProcessor.GetAngularVelocity
---

# IManipulationProcessor::GetAngularVelocity


## -description

The <b>GetAngularVelocity</b> method calculates the rotational velocity that the target object is moving at.

## -parameters

### -param angularVelocity [out]

The calculated rotational velocity.

## -returns

Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.

## -remarks

This value is useful when you are setting up the initial state of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.

This property is expressed in radians per millisecond if explicit timestamps are not specified by using calls to <a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime">ProcessMoveWithTime</a>, <b>ProcessMoveWithTime</b>, and <a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime">ProcessUpWithTime</a>. Otherwise, this function uses radians per user defined time units.

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity">InitialAngularVelocity</a>



<a href="/windows/desktop/wintouch/mtmethods">Methods</a>