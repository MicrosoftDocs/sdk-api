---
UID: NF:setupapi.SetupDiGetClassImageIndex
title: SetupDiGetClassImageIndex function
author: windows-sdk-content
description: The SetupDiGetClassImageIndex function retrieves the index within the class image list of a specified class.
old-location: devinst\setupdigetclassimageindex.htm
old-project: devinst
ms.assetid: 56c17b9a-d516-4903-90fc-efac22e1f50d
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: SetupDiGetClassImageIndex, SetupDiGetClassImageIndex function [Device and Driver Installation], devinst.setupdigetclassimageindex, di-rtns_6f022ba0-12d8-47f4-9e7f-27f94dbe9b71.xml, setupapi/SetupDiGetClassImageIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupDiGetClassImageIndex
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiGetClassImageIndex function


## -description


The <b>SetupDiGetClassImageIndex</b> function retrieves the index within the class image list of a specified class.


## -parameters




### -param ClassImageListData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552339">SP_CLASSIMAGELIST_DATA</a> structure that describes a class image list that includes the image for the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> that is specified by the <i>ClassGuid</i> parameter. 


### -param ClassGuid [in]

A pointer to the GUID of the device setup class for which to retrieve the index of the class image in the specified class image list.


### -param ImageIndex [out]

A pointer to an INT-typed variable that receives the index of the specified class image in the class image list.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the specified device setup class is not included in the specified class image list, <b>SetupDiGetClassImageIndex</b> returns the image index for the Unknown device setup class in the <i>ImageIndex</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551080">SetupDiGetClassImageList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551081">SetupDiGetClassImageListEx</a>
 

 

