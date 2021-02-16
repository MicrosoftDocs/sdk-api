---
UID: NF:inkpresenterdesktop.IInkDesktopHost.CreateInkPresenter
title: IInkDesktopHost::CreateInkPresenter (inkpresenterdesktop.h)
description: Creates an IInkPresenterDesktop object on an application thread.
helpviewer_keywords: ["CreateInkPresenter","CreateInkPresenter method","CreateInkPresenter method","IInkDesktopHost interface","IInkDesktopHost interface","CreateInkPresenter method","IInkDesktopHost.CreateInkPresenter","IInkDesktopHost::CreateInkPresenter","InkPresenterDesktop.iinkdesktophost_createinkpresenter","inkpresenterdesktop/IInkDesktopHost::CreateInkPresenter","input_ink.iinkdesktophost_createinkpresenter"]
old-location: input_ink\iinkdesktophost_createinkpresenter.htm
tech.root: input_ink
ms.assetid: 17480bbd-7d4f-4ba9-9d54-80f440104055
ms.date: 12/05/2018
ms.keywords: CreateInkPresenter, CreateInkPresenter method, CreateInkPresenter method,IInkDesktopHost interface, IInkDesktopHost interface,CreateInkPresenter method, IInkDesktopHost.CreateInkPresenter, IInkDesktopHost::CreateInkPresenter, InkPresenterDesktop.iinkdesktophost_createinkpresenter, inkpresenterdesktop/IInkDesktopHost::CreateInkPresenter, input_ink.iinkdesktophost_createinkpresenter
req.header: inkpresenterdesktop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InkPresenterDesktop.idl
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
 - IInkDesktopHost::CreateInkPresenter
 - inkpresenterdesktop/IInkDesktopHost::CreateInkPresenter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkPresenterDesktop.h
api_name:
 - IInkDesktopHost.CreateInkPresenter
---

# IInkDesktopHost::CreateInkPresenter


## -description

Creates an <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a> object on an application thread.

The <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a> object can then be configured and connected to the app's  <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a> visual tree. 
<div class="alert"><b>Note</b>  <p class="note">Use <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter">CreateAndInitializeInkPresenter</a> to do this in a single call.

</div><div> </div>

## -parameters

### -param riid [in]

A reference to the interface identifier of an <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a> object.

### -param ppv [out]

Address of a pointer variable that receives the interface pointer identified by <i>riid</i>.

## -returns

If successful, returns the requested interface pointer. Otherwise, returns <b>NULL</b>.

## -see-also

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex ink sample</a>



<a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost">IInkDesktopHost</a>






<a href="/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>

<a href="https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex Ink sample</a>

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk">Simple ink sample</a>