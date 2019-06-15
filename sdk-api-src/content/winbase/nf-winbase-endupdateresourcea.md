---
UID: NF:winbase.EndUpdateResourceA
title: EndUpdateResourceA function (winbase.h)
author: windows-sdk-content
description: Commits or discards changes made prior to a call to UpdateResource.
old-location: menurc\endupdateresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\endupdateresource.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndUpdateResource, EndUpdateResource function [Menus and Other Resources], EndUpdateResourceA, EndUpdateResourceW, _win32_EndUpdateResource, _win32_endupdateresource_cpp, menurc.endupdateresource, winbase/EndUpdateResource, winbase/EndUpdateResourceA, winbase/EndUpdateResourceW, winui._win32_endupdateresource
ms.topic: function
f1_keywords: ["winbase/EndUpdateResource"]
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EndUpdateResourceW (Unicode) and EndUpdateResourceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - EndUpdateResource
 - EndUpdateResourceA
 - EndUpdateResourceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EndUpdateResourceA function


## -description


Commits or discards changes made prior to a call to <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a>.


## -parameters




### -param hUpdate [in]

Type: <b>HANDLE</b>

A module handle returned by the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-beginupdateresourcea">BeginUpdateResource</a> function, and used by <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a>, referencing the file to be updated. 


### -param fDiscard [in]

Type: <b>BOOL</b>

Indicates whether to write the resource updates to the file. If this parameter is <b>TRUE</b>, no changes are made. If it is <b>FALSE</b>, the changes are made: the resource updates will take effect. 


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the function succeeds; <b>FALSE</b> otherwise. If the function succeeds and 

<i>fDiscard</i> is <b>TRUE</b>, then no resource updates are made to the file; otherwise all 

successful resource updates are made to the file. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Before you call this function, make sure all file handles other than the one returned by <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-beginupdateresourcea">BeginUpdateResource</a> are closed.

This function can update resources within modules that contain both code and resources. There are restrictions on resource updates in LN files and .mui files, both of which contain Resource Configuration data; details of the restrictions are in the reference for the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a> function.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/menurc/using-resources">Updating Resources</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-beginupdateresourcea">BeginUpdateResource</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/resources">Resources</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a>
 

 

