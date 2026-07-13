---
UID: NF:wmnetsourcecreator.INSNetSourceCreator.Shutdown
title: INSNetSourceCreator::Shutdown (wmnetsourcecreator.h)
description: The Shutdown method properly disposes of all allocated memory used by the network source creator. You must call this method when you are finished using the network source creator, to ensure that all resources are released.
helpviewer_keywords: ["INSNetSourceCreator interface [windows Media Format]","Shutdown method","INSNetSourceCreator.Shutdown","INSNetSourceCreator::Shutdown","INSNetSourceCreatorShutdown","Shutdown","Shutdown method [windows Media Format]","Shutdown method [windows Media Format]","INSNetSourceCreator interface","wmformat.insnetsourcecreator_shutdown","wmnetsourcecreator/INSNetSourceCreator::Shutdown"]
old-location: wmformat\insnetsourcecreator_shutdown.htm
tech.root: wmformat
ms.assetid: 746b2ffa-c5bc-4df0-84fd-c3f1395e0d3e
ms.date: 4/26/2023
ms.keywords: INSNetSourceCreator interface [windows Media Format],Shutdown method, INSNetSourceCreator.Shutdown, INSNetSourceCreator::Shutdown, INSNetSourceCreatorShutdown, Shutdown, Shutdown method [windows Media Format], Shutdown method [windows Media Format],INSNetSourceCreator interface, wmformat.insnetsourcecreator_shutdown, wmnetsourcecreator/INSNetSourceCreator::Shutdown
req.header: wmnetsourcecreator.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INSNetSourceCreator::Shutdown
 - wmnetsourcecreator/INSNetSourceCreator::Shutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - INSNetSourceCreator.Shutdown
---

# INSNetSourceCreator::Shutdown


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Shutdown</b> method properly disposes of all allocated memory used by the network source creator. You must call this method when you are finished using the network source creator, to ensure that all resources are released.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmnetsourcecreator/nn-wmnetsourcecreator-insnetsourcecreator">INSNetSourceCreator Interface</a>



<a href="/windows/desktop/api/wmnetsourcecreator/nf-wmnetsourcecreator-insnetsourcecreator-initialize">INSNetSourceCreator::Initialize</a>
