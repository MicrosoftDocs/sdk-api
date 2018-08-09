---
UID: NF:roapi.RoUninitialize
title: RoUninitialize function
author: windows-sdk-content
description: Closes the Windows Runtime on the current thread.
old-location: winrt\rouninitialize.htm
old-project: WinRT
ms.assetid: 0F910E71-BA44-44A6-8432-52A4E38854F9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RoUninitialize, RoUninitialize function [Windows Runtime], WinRTUninitialize, roapi/RoUninitialize, roapi/WinRTUninitialize, winrt.rouninitialize, winrt.winrtuninitialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: RO_INIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - roapi.h
 - API-MS-Win-Core-WinRT-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoUninitialize
 - WinRTUninitialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# RoUninitialize function


## -description


Closes the Windows Runtime on the current thread.


## -parameters






## -returns



This function does not return a value.




## -remarks



Call the <b>RoUninitialize</b> function to close the Windows Runtime on the current thread. This unloads all DLLs loaded by the thread, frees any other resources that the thread maintains, and forces all RPC connections on the thread to close.

Use the <a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a> function to initialize a thread in the Windows Runtime.  






## -see-also




<a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>



<a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a>
 

 

