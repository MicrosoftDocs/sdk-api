---
UID: NF:activationregistration.IExeServerRegistration.get_CommandLine
title: IExeServerRegistration::get_CommandLine (activationregistration.h)
description: Gets the command line used to launch the out-of-process server.
helpviewer_keywords: ["IExeServerRegistration interface [Windows Runtime]","get_CommandLine method","IExeServerRegistration.get_CommandLine","IExeServerRegistration::get_CommandLine","activationregistration/IExeServerRegistration::get_CommandLine","get_CommandLine","get_CommandLine method [Windows Runtime]","get_CommandLine method [Windows Runtime]","IExeServerRegistration interface","winrt.iexeserverregistration_commandline"]
old-location: winrt\iexeserverregistration_commandline.htm
tech.root: WinRT
ms.assetid: 2A4B80B9-3590-411C-8834-6850A44AF46C
ms.date: 12/05/2018
ms.keywords: IExeServerRegistration interface [Windows Runtime],get_CommandLine method, IExeServerRegistration.get_CommandLine, IExeServerRegistration::get_CommandLine, activationregistration/IExeServerRegistration::get_CommandLine, get_CommandLine, get_CommandLine method [Windows Runtime], get_CommandLine method [Windows Runtime],IExeServerRegistration interface, winrt.iexeserverregistration_commandline
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IExeServerRegistration::get_CommandLine
 - activationregistration/IExeServerRegistration::get_CommandLine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - activationregistration.h
api_name:
 - IExeServerRegistration.get_CommandLine
---

# IExeServerRegistration::get_CommandLine


## -description

Gets the command line used to launch the out-of-process server.

## -parameters

### -param commandLine [out, retval]

The command line used to launch the out-of-process server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserverregistration">IExeServerRegistration</a>