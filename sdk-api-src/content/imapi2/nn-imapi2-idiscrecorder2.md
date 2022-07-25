---
UID: NN:imapi2.IDiscRecorder2
title: IDiscRecorder2 (imapi2.h)
description: This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or eject the media.
helpviewer_keywords: ["IDiscRecorder2","IDiscRecorder2 interface [IMAPI]","IDiscRecorder2 interface [IMAPI]","described","imapi.idiscrecorder2","imapi2/IDiscRecorder2"]
old-location: imapi\idiscrecorder2.htm
tech.root: imapi
ms.assetid: 34f858b8-74eb-4725-8815-7954cb98cff0
ms.date: 12/05/2018
ms.keywords: IDiscRecorder2, IDiscRecorder2 interface [IMAPI], IDiscRecorder2 interface [IMAPI],described, imapi.idiscrecorder2, imapi2/IDiscRecorder2
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
 - IDiscRecorder2
 - imapi2/IDiscRecorder2
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
 - IDiscRecorder2
---

# IDiscRecorder2 interface


## -description

This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or eject the media.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscRecorder2) for the class identifier and __uuidof(IDiscRecorder2) for the interface identifier.

## -inheritance

The <b>IDiscRecorder2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDiscRecorder2</b> also has these types of members:

## -remarks

To create the <b>MsftDiscRecorder2</b> object in a script, use IMAPI2.MsftDiscRecorder2 as the program identifier when calling <b>CreateObject</b>.

To write data to media, you need to attach a recorder to a format writer, for example, to attach the recorder to a data writer, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder">IDiscFormat2Data::put_Recorder</a> method.

Several properties of this interface return packet data defined by Multimedia Command (MMC). For information on the format of the packet data, see the latest revision of the MMC specification at ftp://ftp.t10.org/t10/drafts/mmc5.

## -see-also

IDiscRecorder2Ex
