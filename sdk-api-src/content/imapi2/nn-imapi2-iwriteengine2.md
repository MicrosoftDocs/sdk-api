---
UID: NN:imapi2.IWriteEngine2
title: IWriteEngine2 (imapi2.h)
description: Use this interface to write a data stream to a device.
helpviewer_keywords: ["IWriteEngine2","IWriteEngine2 interface [IMAPI]","IWriteEngine2 interface [IMAPI]","described","imapi.iwriteengine2","imapi2/IWriteEngine2"]
old-location: imapi\iwriteengine2.htm
tech.root: imapi
ms.assetid: 89e7526f-2b9b-4f37-b537-5046a0ac283d
ms.date: 12/05/2018
ms.keywords: IWriteEngine2, IWriteEngine2 interface [IMAPI], IWriteEngine2 interface [IMAPI],described, imapi.iwriteengine2, imapi2/IWriteEngine2
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
 - IWriteEngine2
 - imapi2/IWriteEngine2
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
 - IWriteEngine2
---

# IWriteEngine2 interface


## -description

Use this interface to write a data stream to a device.

This interface should be used by those  developing support for new media types or formats. Writing to media typically includes the following steps:<ol>
<li>Preparing the hardware by setting mode pages for the media.
</li>
<li>Querying the hardware to verify that the media is large enough.</li>
<li>Initializing the write, for example, by formatting the media or setting OPC.
</li>
<li>Performing the actual WRITE commands.</li>
<li>Finishing the write by stopping the formatting or closing the session or track.</li>
</ol>When developing support for new media types, you can implement steps 1, 2, 3, and 5, and use this interface to perform step 4. Note that all the IDiscFormat2* interfaces use this interface to perform the write operation.

Most client applications should use the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a> interface to write images to a device.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftWriteEngine2) for the class identifier and __uuidof(IWriteEngine2) for the interface identifier.

## -inheritance

The <b>IWriteEngine2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWriteEngine2</b> also has these types of members:

## -remarks

To create the <b>MsftWriteEngine2</b> object in a script, use IMAPI2.MsftWriteEngine2 as the program identifier when calling <b>CreateObject</b>.

 It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="/windows/desktop/imapi/preventing-logoff-or-suspend-during-a-burn">Preventing Logoff or Suspend During a Burn</a>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events">DWriteEngine2Events</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>
