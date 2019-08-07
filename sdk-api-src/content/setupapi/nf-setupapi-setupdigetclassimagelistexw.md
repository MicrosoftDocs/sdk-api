---
UID: NF:setupapi.SetupDiGetClassImageListExW
title: SetupDiGetClassImageListExW function (setupapi.h)
author: windows-sdk-content
description: The SetupDiGetClassImageListEx function builds an image list of bitmaps for every class installed on a local or remote system.
old-location: devinst\setupdigetclassimagelistex.htm
tech.root: devinst
ms.assetid: f9cf7904-3fda-4f7f-bb05-3634fd1c9af3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassImageListEx, SetupDiGetClassImageListEx function [Device and Driver Installation], SetupDiGetClassImageListExA, SetupDiGetClassImageListExW, devinst.setupdigetclassimagelistex, di-rtns_ff251460-9ebf-4968-80f2-f44c13305197.xml, setupapi/SetupDiGetClassImageListEx
ms.topic: function
f1_keywords:
- setupapi/SetupDiGetClassImageListEx
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- Setupapi.lib
- Setupapi.dll
api_name:
- SetupDiGetClassImageListEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiGetClassImageListExW function


## -description


The <b>SetupDiGetClassImageListEx</b> function builds an image list of bitmaps for every class installed on a local or remote system.


## -parameters




### -param ClassImageListData [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_classimagelist_data">SP_CLASSIMAGELIST_DATA</a> structure to receive information regarding the class image list, including a handle to the image list. The <b>cbSize</b> field of this structure must be initialized with the size of the structure, in bytes, before calling this function or it will fail.


### -param MachineName [in, optional]

A pointer to NULL-terminated string that supplies the name of a remote system for whose classes <b>SetupDiGetClassImageListEx must build </b>the bitmap. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, <b>SetupDiGetClassImageListEx</b> builds the list for the local system.


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The image list built by this function should be destroyed by calling <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdidestroyclassimagelist">SetupDiDestroyClassImageList</a>.

<div class="alert"><b>Note</b>    Class-specific icons on a remote computer can only be displayed if the class is also present on the local computer. Thus, if the remote computer has class <i>X</i>, but class <i>X</i> is not installed locally, then the generic (unknown) icon will be returned.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdidestroyclassimagelist">SetupDiDestroyClassImageList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelist">SetupDiGetClassImageList</a>
 

 

