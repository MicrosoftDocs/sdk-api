---
UID: NF:mfidl.MFCreateContentProtectionDevice
title: MFCreateContentProtectionDevice function
author: windows-sdk-content
description: Creates an IMFContentProtectionDevice interface for the specified media protection system.
old-location: mf\mfcreatecontentprotectiondevice.htm
tech.root: medfound
ms.assetid: 6C301184-255B-4FE7-8DD6-962B236F90A6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFCreateContentProtectionDevice, MFCreateContentProtectionDevice function [Media Foundation], mf.mfcreatecontentprotectiondevice, mfidl/MFCreateContentProtectionDevice
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateContentProtectionDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateContentProtectionDevice function


## -description


Creates an <a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a> interface for the specified media protection system.


## -parameters




### -param ProtectionSystemId [in]

The idenfier of the media protection system for which you want to create the <a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a> interface.


### -param ContentProtectionDevice [out]

Pointer to the created <a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

