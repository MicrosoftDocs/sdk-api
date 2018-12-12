---
UID: NF:wmsdkidl.IWMWriterFileSink3.OnDataUnitEx
title: IWMWriterFileSink3::OnDataUnitEx
author: windows-sdk-content
description: The OnDataUnitEx method is called when the writer has finished sending a data unit.
old-location: wmformat\iwmwriterfilesink3_ondataunitex.htm
tech.root: wmformat
ms.assetid: 1dbcb27b-7588-4475-99fe-3e547d1659d3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterFileSink3 interface [windows Media Format],OnDataUnitEx method, IWMWriterFileSink3.OnDataUnitEx, IWMWriterFileSink3::OnDataUnitEx, IWMWriterFileSink3OnDataUnitEx, OnDataUnitEx, OnDataUnitEx method [windows Media Format], OnDataUnitEx method [windows Media Format],IWMWriterFileSink3 interface, wmformat.iwmwriterfilesink3_ondataunitex, wmsdkidl/IWMWriterFileSink3::OnDataUnitEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
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
 - IWMWriterFileSink3.OnDataUnitEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterFileSink3::OnDataUnitEx


## -description



The <b>OnDataUnitEx</b> method is called when the writer has finished sending a data unit.



<b>OnDataUnitEx</b> is an enhanced version of <a href="https://msdn.microsoft.com/en-us/library/Dd757470(v=VS.85).aspx">IWMWriterSink::OnDataUnit</a>. The difference between these two methods is that <b>OnDataUnitEx</b> delivers very granular data unit information. You can examine individual payload headers, payload data fragments, and the packet header.


## -parameters




### -param pFileSinkDataUnit [in]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd757841(v=VS.85).aspx">WMT_FILESINK_DATA_UNIT</a> structure containing the data unit information.


## -returns



This method always returns S_OK.




## -remarks



Applications do not call this method. If you are implementing the <b>IWMWriterFileSink3</b> interface on a custom sink, you have the option of implementing this method. If you do so, your implementation of <a href="https://msdn.microsoft.com/en-us/library/Dd798754(v=VS.85).aspx">GetMode</a> should return WMT_FM_FILESINK_DATA_UNITS.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798751(v=VS.85).aspx">IWMWriterFileSink3 Interface</a>
 

 

