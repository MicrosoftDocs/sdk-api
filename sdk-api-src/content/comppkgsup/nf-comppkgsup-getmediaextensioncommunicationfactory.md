---
UID: NF:comppkgsup.GetMediaExtensionCommunicationFactory
title: GetMediaExtensionCommunicationFactory function
author: windows-sdk-content
description: Creates a communication factory for registering a media extension.
old-location: winprog\getmediaextensioncommunicationfactory.htm
tech.root: devnotes
ms.assetid: 79186891-FD54-4498-AF2A-D79D30F859A2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMediaExtensionCommunicationFactory, GetMediaExtensionCommunicationFactory function [Windows API], comppkgsup/GetMediaExtensionCommunicationFactory, winprog.getmediaextensioncommunicationfactory
ms.topic: function
req.header: comppkgsup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comppkgsup.lib
req.dll: CompPkgSup.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CompPkgSup.dll
api_name:
 - GetMediaExtensionCommunicationFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMediaExtensionCommunicationFactory function


## -description


Creates a communication factory for registering a media extension.


## -parameters




### -param factory [out]

The communication factory.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use this API to create and hold a reference count on  the communication factory. Once the call to <b>RegisterMediaExtensionForAppService</b> has been made the  reference count on the communication factory can be released. 



