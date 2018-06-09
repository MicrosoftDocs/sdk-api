---
UID: NF:mfidl.MFCreateTranscodeSinkActivate
title: MFCreateTranscodeSinkActivate function
author: windows-sdk-content
description: Creates the transcode sink activation object.
old-location: mf\mfcreatetranscodesinkactivate.htm
old-project: medfound
ms.assetid: cc9c604d-7f5a-4afb-a2df-b270ef883e68
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCreateTranscodeSinkActivate, MFCreateTranscodeSinkActivate function [Media Foundation], mf.mfcreatetranscodesinkactivate, mfidl/MFCreateTranscodeSinkActivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mf.dll
api_name:
 - MFCreateTranscodeSinkActivate
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateTranscodeSinkActivate function


## -description


Creates the transcode sink activation object.

The transcode sink activation object can be used to create any of the following file sinks:
<ul>
<li>3GP file sink</li>
<li>MP3 file sink</li>
<li>MP4 file sink</li>
</ul>The transcode sink activation object exposes the <a href="https://msdn.microsoft.com/c5eb0c30-559a-44dd-80d4-4b11933dc7ce">IMFTranscodeSinkInfoProvider</a> interface.


## -parameters




### -param ppActivate [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface. This interface is used to create the file sink instance from the activation object. Before doing so, query the returned pointer for the <a href="https://msdn.microsoft.com/c5eb0c30-559a-44dd-80d4-4b11933dc7ce">IMFTranscodeSinkInfoProvider</a> interface and use that interface to initialize the object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c5eb0c30-559a-44dd-80d4-4b11933dc7ce">IMFTranscodeSinkInfoProvider</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

