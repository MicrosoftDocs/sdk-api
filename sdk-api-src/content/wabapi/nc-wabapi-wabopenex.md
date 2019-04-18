---
UID: NC:wabapi.WABOpenEx
title: WABOpenEx (wabapi.h)
author: windows-sdk-content
description: WABOpenEx is no longer available for use as of Windows Vista.
old-location: wab\_wab_WABOpenEx.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\functions\wabopenex.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WABOpenEx, WABOpenEx callback, WABOpenEx callback function [Windows Address Book], _wab_WABOpenEx, wab._wab_WABOpenEx, wabapi/WABOpenEx
ms.topic: callback
req.header: wabapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wabapi.h
api_name:
 - WABOpenEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.5
ms.custom: 19H1
---

# WABOpenEx callback function


## -description


<p class="CCE_Message">[<i>WABOpenEx</i> is no longer available for use as of Windows Vista.]

Provides access to the Windows Address Book (WAB) through a number of object interfaces. The root interface is <a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a>, which is a subset of the MAPI implementation of <a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a>.


## -parameters




### -param lppAdrBook

Type: <b>LPADRBOOK*</b>

Address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a> interface returned by the function.


### -param lppWABObject

Type: <b>LPWABOBJECT*</b>

Address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms629467(v=VS.85).aspx">IWABObject</a> interface returned by the function.


### -param lpWP


### -param Reserved


### -param fnAllocateBuffer


### -param fnAllocateMore


### -param fnFreeBuffer








#### - Reserved2

Type: <b>DWORD</b>

Reserved. Must be set to 0.


#### - lpWABParam

Type: <b>LPWAB_PARAM</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms629458(v=VS.85).aspx">WAB_PARAM</a> structure. Supported by Internet Explorer 4.0 or later.


#### - lpfnAllocateBuffer

Type: <b>ALLOCATEBUFFER*</b>

Pointer to a function that specifies the <a href="https://msdn.microsoft.com/library/ms528639(v=EXCHG.10).aspx">MAPIAllocateBuffer</a>-style allocation function. Set to <b>NULL</b> to use WAB internal routines.


#### - lpfnAllocateMore

Type: <b>ALLOCATEMORE*</b>

Pointer to a function that specifies the <a href="https://msdn.microsoft.com/library/ms528603(v=EXCHG.10).aspx">MAPIAllocateMore</a>-style allocation function. Set to <b>NULL</b> to use WAB internal routines.


#### - lpfnFreeBuffer

Type: <b>FREEBUFFER*</b>

Pointer to a function that specifies the <a href="https://msdn.microsoft.com/en-us/library/Dd296736(v=VS.85).aspx">MAPIFreeBuffer</a>-style memory freeing function. Set to <b>NULL</b> to use WAB internal routines.


## -returns



Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function calls the <a href="https://msdn.microsoft.com/en-us/library/ms629715(v=VS.85).aspx">WABOpen</a> function, and the extra parameters <i>lpfnAllocateBuffer</i>, <i>lpfnAllocateMore</i>, and <i>lpfnFreeBuffer</i> are ignored.

<i>WABOpenEx</i> is an extended version of <a href="https://msdn.microsoft.com/en-us/library/ms629715(v=VS.85).aspx">WABOpen</a> that enables developers to specify the memory allocation functions used by WAB to return buffers to the client. If you pass one allocation routine, you must pass all three routines: <a href="https://msdn.microsoft.com/library/ms528639(v=EXCHG.10).aspx">MAPIAllocateBuffer</a>, <a href="https://msdn.microsoft.com/library/ms528603(v=EXCHG.10).aspx">MAPIAllocateMore</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd296736(v=VS.85).aspx">MAPIFreeBuffer</a>.

If you do not need the extra memory allocation functionality of <i>WABOpenEx</i>, use <a href="https://msdn.microsoft.com/en-us/library/ms629715(v=VS.85).aspx">WABOpen</a> instead.

<div class="alert"><b>Note</b>  When you specify memory allocation routines with <i>WABOpenEx</i>, these routines globally replace the WAB internal routines for this process.  Other threads may still call <a href="https://msdn.microsoft.com/en-us/library/ms629715(v=VS.85).aspx">WABOpen</a>, but the memory will be allocated with those routines previously passed to <i>WABOpenEx</i>.  
</div>
<div> </div>


