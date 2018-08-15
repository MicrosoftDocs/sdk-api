---
UID: NF:ole2.OleUninitialize
title: OleUninitialize function
author: windows-sdk-content
description: Closes the COM library on the apartment, releases any class factories, other COM objects, or servers held by the apartment, disables RPC on the apartment, and frees any resources the apartment maintains.
old-location: com\oleuninitialize.htm
old-project: com
ms.assetid: b2a8233f-7e1b-4c54-9363-7478c40c3830
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OleUninitialize, OleUninitialize function [COM], _ole_OleUninitialize, com.oleuninitialize, ole2/OleUninitialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleUninitialize
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleUninitialize function


## -description


Closes the COM library on the apartment, releases any class factories, other COM objects, or servers held by the apartment, disables RPC on the apartment, and frees any resources the apartment maintains.




## -parameters






## -returns



This function does not return a value.




## -remarks



Call <b>OleUninitialize</b> on application shutdown, as the last COM library call, if the apartment was initialized with a call to <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a>. <b>OleUninitialize</b> calls the <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> function internally to shut down the OLE Component Object(COM) Library.

If the COM library was initialized on the apartment with a call to <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>, it must be closed with a call to <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>.

The <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> and <b>OleUninitialize</b> calls must be balanced â€” if there are multiple calls to the <b>OleInitialize</b> function, there must be the same number of calls to <b>OleUninitialize</b>; only the <b>OleUninitialize</b> call corresponding to the <b>OleInitialize</b> call that actually initialized the library can close it.

Because there is no way to control the order in which in-process servers are loaded or unloaded, do not call <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> or <b>OleUninitialize</b> from the <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a>



<a href="https://msdn.microsoft.com/b2a8233f-7e1b-4c54-9363-7478c40c3830">OleUninitialize</a>
 

 

