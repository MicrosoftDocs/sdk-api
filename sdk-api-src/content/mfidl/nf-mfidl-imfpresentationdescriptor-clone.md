---
UID: NF:mfidl.IMFPresentationDescriptor.Clone
title: IMFPresentationDescriptor::Clone
author: windows-sdk-content
description: Creates a copy of this presentation descriptor.
old-location: mf\imfpresentationdescriptor_clone.htm
old-project: medfound
ms.assetid: 084b3adf-092a-4869-92e1-982db209bd5b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 084b3adf-092a-4869-92e1-982db209bd5b, Clone, Clone method [Media Foundation], Clone method [Media Foundation],IMFPresentationDescriptor interface, IMFPresentationDescriptor interface [Media Foundation],Clone method, IMFPresentationDescriptor.Clone, IMFPresentationDescriptor::Clone, mf.imfpresentationdescriptor_clone, mfidl/IMFPresentationDescriptor::Clone
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
 - IMFPresentationDescriptor.Clone
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPresentationDescriptor::Clone


## -description



Creates a copy of this presentation descriptor.




## -parameters




### -param ppPresentationDescriptor [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface of the new presentation descriptor. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        This method performs a shallow copy of the presentation descriptor. The stream descriptors are not cloned. Therefore, use caution when modifying the presentation presentation descriptor or its stream descriptors.
      


        If the original presentation descriptor is from a media source, do not modify the presentation descriptor unless the source is stopped. If you use the presentation descriptor to configure a media sink, do not modify the presentation descriptor after the sink is configured.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

