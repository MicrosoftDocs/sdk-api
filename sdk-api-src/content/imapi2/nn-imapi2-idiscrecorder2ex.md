---
UID: NN:imapi2.IDiscRecorder2Ex
title: IDiscRecorder2Ex (imapi2.h)
description: This interface represents a physical device.
helpviewer_keywords: ["IDiscRecorder2Ex","IDiscRecorder2Ex interface [IMAPI]","IDiscRecorder2Ex interface [IMAPI]","described","imapi.idiscrecorder2ex","imapi2/IDiscRecorder2Ex"]
old-location: imapi\idiscrecorder2ex.htm
tech.root: imapi
ms.assetid: 37e65b57-ec53-405c-a7bd-34c2df15d5d7
ms.date: 12/05/2018
ms.keywords: IDiscRecorder2Ex, IDiscRecorder2Ex interface [IMAPI], IDiscRecorder2Ex interface [IMAPI],described, imapi.idiscrecorder2ex, imapi2/IDiscRecorder2Ex
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
 - IDiscRecorder2Ex
 - imapi2/IDiscRecorder2Ex
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
 - IDiscRecorder2Ex
---

# IDiscRecorder2Ex interface


## -description

This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or ejecting the media. This interface retrieves information not available through <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface, and provides easier access to some of the same property values in <b>IDiscRecorder2</b>.

To get an instance of this interface, create an instance of the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface and then call the <b>IDiscRecorder2::QueryInterface</b> method to retrieve the <b>IDiscRecorder2Ex</b> interface.

Note that you cannot access this functionality from script.

## -inheritance

The <b>IDiscRecorder2Ex</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDiscRecorder2Ex</b> also has these types of members:

## -remarks

To write data to media, you need to attach this recorder to the <a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a> data writer, using the <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_recorder">IWriteEngine2::put_Recorder</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a>
