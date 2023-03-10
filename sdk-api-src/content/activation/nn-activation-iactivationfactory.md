---
UID: NN:activation.IActivationFactory
title: IActivationFactory (activation.h)
description: Enables classes to be activated by the Windows Runtime.
helpviewer_keywords: ["IActivationFactory","IActivationFactory interface [Windows Runtime]","IActivationFactory interface [Windows Runtime]","described","activation/IActivationFactory","winrt.iactivationfactory"]
old-location: winrt\iactivationfactory.htm
tech.root: WinRT
ms.assetid: C6A2ED6E-9C45-4CF3-A301-72A5DAEB4DFC
ms.date: 12/05/2018
ms.keywords: IActivationFactory, IActivationFactory interface [Windows Runtime], IActivationFactory interface [Windows Runtime],described, activation/IActivationFactory, winrt.iactivationfactory
req.header: activation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Activation.idl
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
 - IActivationFactory
 - activation/IActivationFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activation.h
api_name:
 - IActivationFactory
---

# IActivationFactory interface


## -description

Enables classes to be activated by the Windows Runtime.

## -inheritance

The <b>IActivationFactory</b> interface inherits from <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IActivationFactory</b> also has these types of members:

## -remarks

Implement the <b>IActivationFactory</b> interface when you create a class that you want Windows Runtime  applications to use. Clients call the <a href="/windows/desktop/api/activation/nf-activation-iactivationfactory-activateinstance">ActivateInstance</a> method to use an instance of your class. 

You can get an <b>IActivationFactory</b> pointer by calling the <a href="/windows/desktop/api/roapi/nf-roapi-rogetactivationfactory">RoGetActivationFactory</a> function.  

During activation of a class, the Windows Runtime calls the <a href="/previous-versions/br205771(v=vs.85)">DllGetActivationFactory</a> function to get an <b>IActivationFactory</b> pointer that corresponds to the requested class.

## -see-also

<a href="/previous-versions/br205771(v=vs.85)">DllGetActivationFactory</a>



<a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>



<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>



<a href="/windows/desktop/api/roapi/nf-roapi-rogetactivationfactory">RoGetActivationFactory</a>
