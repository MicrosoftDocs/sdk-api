---
UID: NF:setupapi.SetupDiGetClassImageIndex
title: SetupDiGetClassImageIndex function (setupapi.h)
author: windows-sdk-content
description: The SetupDiGetClassImageIndex function retrieves the index within the class image list of a specified class.
old-location: devinst\setupdigetclassimageindex.htm
tech.root: devinst
ms.assetid: 56c17b9a-d516-4903-90fc-efac22e1f50d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassImageIndex, SetupDiGetClassImageIndex function [Device and Driver Installation], devinst.setupdigetclassimageindex, di-rtns_6f022ba0-12d8-47f4-9e7f-27f94dbe9b71.xml, setupapi/SetupDiGetClassImageIndex
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# SetupDiGetClassImageIndex function


## -description


The <b>SetupDiGetClassImageIndex</b> function retrieves the index within the class image list of a specified class.


## -parameters




### -param ClassImageListData [in]

A pointer to an <a href="https://msdn.microsoft.com/89ed9dbd-3c5e-43ff-bbd0-fd6cc8c6e6ab">SP_CLASSIMAGELIST_DATA</a> structure that describes a class image list that includes the image for the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> that is specified by the <i>ClassGuid</i> parameter. 


### -param ClassGuid [in]

A pointer to the GUID of the device setup class for which to retrieve the index of the class image in the specified class image list.


### -param ImageIndex [out]

A pointer to an INT-typed variable that receives the index of the specified class image in the class image list.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the specified device setup class is not included in the specified class image list, <b>SetupDiGetClassImageIndex</b> returns the image index for the Unknown device setup class in the <i>ImageIndex</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/d6b84403-9284-4fba-a419-a013cf68ea1e">SetupDiGetClassImageList</a>



<a href="https://msdn.microsoft.com/f9cf7904-3fda-4f7f-bb05-3634fd1c9af3">SetupDiGetClassImageListEx</a>
 

 

