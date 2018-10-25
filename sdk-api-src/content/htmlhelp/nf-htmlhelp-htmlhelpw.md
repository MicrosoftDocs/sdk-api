---
UID: NF:htmlhelp.HtmlHelpW
title: HtmlHelpW function
author: windows-sdk-content
description: Displays a help window.
old-location: htmlhelp\htmlhelp.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconhowcallingthehtmlhelpapi.htm
ms.author: windowssdkdev
ms.date: 10/22/2018
ms.keywords: HtmlHelp, HtmlHelp function [HTML Help Workshop], HtmlHelpA, HtmlHelpW, htmlhelp.htmlhelp, htmlhelp/HtmlHelp, htmlhelp/HtmlHelpA, htmlhelp/HtmlHelpW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: htmlhelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HtmlHelpW (Unicode) and HtmlHelpA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Htmlhelp.lib
req.dll: Htmlhelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Htmlhelp.dll
api_name:
 - HtmlHelp
 - HtmlHelpA
 - HtmlHelpW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HtmlHelpW function


## -description


Displays a help window.

Using the API commands, you can specify which topic to display in the help window, whether the help window is a three-pane Help Viewer or a pop-up window, and whether the HTML topic file should be accessed via a context ID, an <a href="https://msdn.microsoft.com/DB3F1302-6933-45e8-9AF7-E3C075549B51">HTML Help URL</a>, or a Keyword link (KLink) lookup. 


## -parameters




### -param hwndCaller [in, optional]

Specifies the handle (<i>hwnd</i>) of the window calling <b>HtmlHelp</b>. The help window is owned by this window. 



When the help window is closed, <b>HtmlHelp</b> will return focus to the owner unless the owner is the desktop. If <i>hwndCaller</i> is the desktop, then the operating system determines where focus is returned.

In addition, if <b>HtmlHelp</b> sends any notification messages from the help window, they are sent to <i>hwndCaller</i> as long as you have enabled <a href="https://msdn.microsoft.com/C2A026AF-C759-4c72-8B7F-3848368E9AA6">notification message</a> tracking in the help window definition.


### -param pszFile [in]

Depending on the <i>uCommand</i> value, specifies the <a href="https://msdn.microsoft.com/DB3F1302-6933-45e8-9AF7-E3C075549B51">file path</a> to either a compiled help (.chm) file, or a topic file within a specified help file. 



A <a href="https://msdn.microsoft.com/4A4AA861-03C6-4c7b-93DB-A10B84F64CC0">window type</a> name can also be specified, preceded with a greater-than (&gt;) character.

If the specified command does not require a file, this value may be NULL.


### -param uCommand [in]

Specifies the <a href="https://msdn.microsoft.com/F5919FDD-48CD-48f2-B8F1-DBEAD660C447">command</a> to complete.


### -param dwData [in]

Specifies any data that may be required, based on the value of the <i>uCommand</i> parameter.


## -returns



Depending on the specified <i>uCommand</i> and the result, <b>HtmlHelp</b> returns one or both of the following: 

<ul>
<li>The handle (hwnd) of the help window.</li>
<li>NULL. In some cases, NULL indicates failure; in other cases, NULL indicates that the help window has not yet been created. </li>
</ul>



## -remarks



The  syntax applies to ANSI character sets.  When using a Unicode character set, the type of the <i>pszFile</i> parameter should be "LPCTSTR  ".

When using the HTML Help API, set the stack size of the hosting executable to at least 100k. If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and failure could result. Optionally, you can remove /STACK from the link command line, and remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case). You can also you can set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).


#### Examples

The following example calls the <a href="https://msdn.microsoft.com/EE933BFD-0C55-47ef-B90B-30250A096CEF">HH_DISPLAY_TOPIC</a> command to open the help file named Help.chm and display its default topic in the help window named Mainwin. Generally, the help window specified in this command is a standard <a href="https://msdn.microsoft.com/9865D3D7-351D-4df6-B1BC-DAF2D725D298">HTML Help Viewer</a>. 


```
HWND hwnd =
   HtmlHelp(
            GetDesktopWindow(),
            "c:\\Help.chm::/Intro.htm>Mainwin",
            HH_DISPLAY_TOPIC,
            NULL) ;
```





## -see-also




<a href="https://msdn.microsoft.com/F1FC7E13-7A29-45d4-8E2E-F21A3C885D04">About the HTML Help API</a>
 

 

