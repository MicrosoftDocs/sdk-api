---
UID: NF:mfidl.MFCreateStreamDescriptor
title: MFCreateStreamDescriptor function
author: windows-sdk-content
description: Creates a stream descriptor.
old-location: mf\mfcreatestreamdescriptor.htm
old-project: medfound
ms.assetid: 77a63d30-c03f-4339-9db3-eda60db9b194
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 77a63d30-c03f-4339-9db3-eda60db9b194, MFCreateStreamDescriptor, MFCreateStreamDescriptor function [Media Foundation], mf.mfcreatestreamdescriptor, mfidl/MFCreateStreamDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateStreamDescriptor
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateStreamDescriptor function


## -description



          Creates a stream descriptor.
        


## -parameters




### -param dwStreamIdentifier


            Stream identifier.
          


### -param cMediaTypes


            Number of elements in the <i>apMediaTypes</i> array.
          


### -param apMediaTypes


            Pointer to an array of <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface pointers. These pointers are used to initialize the media type handler for the stream descriptor.
          


### -param ppDescriptor


            Receives a pointer to the <a href="https://msdn.microsoft.com/a076dc6e-d9cb-4f7e-8cc2-b66292da295f">IMFStreamDescriptor</a> interface of the new stream descriptor. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        If you are writing a custom media source, you can use this function to create stream descriptors for the source. This function automatically creates the stream descriptor media type handler and initializes it with the list of types given in <i>apMediaTypes</i>. The function does not set the current media type on the handler, however. To set the type, call <a href="https://msdn.microsoft.com/77ff397e-4fa8-4849-98b8-6bdd035c0e89">IMFMediaTypeHandler::SetCurrentMediaType</a>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

