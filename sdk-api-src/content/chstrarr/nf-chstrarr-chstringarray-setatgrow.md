---
UID: NF:chstrarr.CHStringArray.SetAtGrow
title: CHStringArray::SetAtGrow
author: windows-sdk-content
description: Sets the array element at the specified index.
old-location: wmi\chstringarray_setatgrow.htm
old-project: WmiSdk
ms.assetid: 49cc7e6f-2d15-4756-bffd-e21f38b8ce8b
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],SetAtGrow method, CHStringArray.SetAtGrow, CHStringArray::SetAtGrow, SetAtGrow, SetAtGrow method [Windows Management Instrumentation], SetAtGrow method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_setatgrow, chstrarr/CHStringArray::SetAtGrow, wmi.chstringarray_setatgrow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: chstrarr.h
req.include-header: FwCommon.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHStringArray.SetAtGrow
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::SetAtGrow


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetAtGrow</b> method sets the array element at the specified index. The array increases automatically if necessary, adjusting the upper bound to accommodate the new element.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero (0).

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to zero (0). The debug version of the <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

### -param newElement

The object pointer to be added to this array. A <b>NULL</b> value is allowed.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/709bed59-c154-4103-9d38-398945657ec6">CHStringArray::SetAt</a>



<a href="https://msdn.microsoft.com/93b10bef-908e-4c5e-aac3-b13051b2e7c9">CHStringArray::operator []</a>
 

 

