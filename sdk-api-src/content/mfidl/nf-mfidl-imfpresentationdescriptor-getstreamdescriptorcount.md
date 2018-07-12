---
UID: NF:mfidl.IMFPresentationDescriptor.GetStreamDescriptorCount
title: IMFPresentationDescriptor::GetStreamDescriptorCount
author: windows-sdk-content
description: Retrieves the number of stream descriptors in the presentation. Each stream descriptor contains information about one stream in the media source. To retrieve a stream descriptor, call the IMFPresentationDescriptor::GetStreamDescriptorByIndex method.
old-location: mf\imfpresentationdescriptor_getstreamdescriptorcount.htm
old-project: medfound
ms.assetid: a01b8f91-b42a-4910-8afb-6134f5f65759
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetStreamDescriptorCount, GetStreamDescriptorCount method [Media Foundation], GetStreamDescriptorCount method [Media Foundation],IMFPresentationDescriptor interface, IMFPresentationDescriptor interface [Media Foundation],GetStreamDescriptorCount method, IMFPresentationDescriptor.GetStreamDescriptorCount, IMFPresentationDescriptor::GetStreamDescriptorCount, a01b8f91-b42a-4910-8afb-6134f5f65759, mf.imfpresentationdescriptor_getstreamdescriptorcount, mfidl/IMFPresentationDescriptor::GetStreamDescriptorCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPresentationDescriptor.GetStreamDescriptorCount
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPresentationDescriptor::GetStreamDescriptorCount


## -description



Retrieves the number of stream descriptors in the presentation. Each stream descriptor contains information about one stream in the media source. To retrieve a stream descriptor, call the <a href="https://msdn.microsoft.com/1db28049-cd62-4b1b-932b-b4d4e12fd671">IMFPresentationDescriptor::GetStreamDescriptorByIndex</a> method.




## -parameters




### -param pdwDescriptorCount [out]

Receives the number of stream descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

