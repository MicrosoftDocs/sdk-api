---
UID: NF:setupapi.SetupDiDestroyClassImageList
title: SetupDiDestroyClassImageList function (setupapi.h)
author: windows-sdk-content
description: The SetupDiDestroyClassImageList function destroys a class image list that was built by a call to SetupDiGetClassImageList or SetupDiGetClassImageListEx.
old-location: devinst\setupdidestroyclassimagelist.htm
tech.root: devinst
ms.assetid: 47ccc16c-b061-489b-b534-5b5929c5d010
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupDiDestroyClassImageList, SetupDiDestroyClassImageList function [Device and Driver Installation], devinst.setupdidestroyclassimagelist, di-rtns_15428f4d-4785-460b-9da1-746cf2c69159.xml, setupapi/SetupDiDestroyClassImageList
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
 - SetupDiDestroyClassImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiDestroyClassImageList function


## -description


The <b>SetupDiDestroyClassImageList</b> function destroys a class image list that was built by a call to <a href="https://msdn.microsoft.com/d6b84403-9284-4fba-a419-a013cf68ea1e">SetupDiGetClassImageList</a> or <a href="https://msdn.microsoft.com/f9cf7904-3fda-4f7f-bb05-3634fd1c9af3">SetupDiGetClassImageListEx</a>.


## -parameters




### -param ClassImageListData [in]

A pointer to an <a href="https://msdn.microsoft.com/89ed9dbd-3c5e-43ff-bbd0-fd6cc8c6e6ab">SP_CLASSIMAGELIST_DATA</a> structure that contains the class image list to destroy.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/d6b84403-9284-4fba-a419-a013cf68ea1e">SetupDiGetClassImageList</a>



<a href="https://msdn.microsoft.com/f9cf7904-3fda-4f7f-bb05-3634fd1c9af3">SetupDiGetClassImageListEx</a>
 

 

