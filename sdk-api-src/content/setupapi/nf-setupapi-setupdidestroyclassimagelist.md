---
UID: NF:setupapi.SetupDiDestroyClassImageList
title: SetupDiDestroyClassImageList function
author: windows-sdk-content
description: The SetupDiDestroyClassImageList function destroys a class image list that was built by a call to SetupDiGetClassImageList or SetupDiGetClassImageListEx.
old-location: devinst\setupdidestroyclassimagelist.htm
old-project: devinst
ms.assetid: 47ccc16c-b061-489b-b534-5b5929c5d010
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: SetupDiDestroyClassImageList, SetupDiDestroyClassImageList function [Device and Driver Installation], devinst.setupdidestroyclassimagelist, di-rtns_15428f4d-4785-460b-9da1-746cf2c69159.xml, setupapi/SetupDiDestroyClassImageList
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
 - SetupDiDestroyClassImageList
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiDestroyClassImageList function


## -description


The <b>SetupDiDestroyClassImageList</b> function destroys a class image list that was built by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff551080">SetupDiGetClassImageList</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff551081">SetupDiGetClassImageListEx</a>.


## -parameters




### -param ClassImageListData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552339">SP_CLASSIMAGELIST_DATA</a> structure that contains the class image list to destroy.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551080">SetupDiGetClassImageList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551081">SetupDiGetClassImageListEx</a>
 

 

