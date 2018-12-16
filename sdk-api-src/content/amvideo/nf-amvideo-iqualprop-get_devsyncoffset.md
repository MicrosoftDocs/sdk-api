---
UID: NF:amvideo.IQualProp.get_DevSyncOffset
title: IQualProp::get_DevSyncOffset
author: windows-sdk-content
description: The get_DevSyncOffset method retrieves the average time difference between when the video frames should have been displayed and when they actually were.
old-location: dshow\iqualprop_get_devsyncoffset.htm
tech.root: DirectShow
ms.assetid: 69160479-7c72-46ed-9421-2a6c2c2861db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IQualProp interface [DirectShow],get_DevSyncOffset method, IQualProp.get_DevSyncOffset, IQualProp::get_DevSyncOffset, IQualPropget_DevSyncOffset, amvideo/IQualProp::get_DevSyncOffset, dshow.iqualprop_get_devsyncoffset, get_DevSyncOffset, get_DevSyncOffset method [DirectShow], get_DevSyncOffset method [DirectShow],IQualProp interface
ms.topic: method
req.header: amvideo.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IQualProp.get_DevSyncOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQualProp::get_DevSyncOffset


## -description



The <code>get_DevSyncOffset</code> method retrieves the average time difference between when the video frames should have been displayed and when they actually were. This method is the same as the <a href="https://msdn.microsoft.com/en-us/library/Dd376917(v=VS.85).aspx">IQualProp::get_AvgSyncOffset</a> method except that the value returned is calculated as a standard deviation rather than as a simple average.




## -parameters




### -param piDev

Pointer to a value denoting the accuracy of the video frames displayed.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



When playing video from networks, the presentation can often be disrupted by network glitches. For this reason, expressing the accuracy of video frames by a simple average is inappropriate. Looking at a standard deviation provides a better idea of the overall accuracy.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376915(v=VS.85).aspx">IQualProp Interface</a>
 

 

