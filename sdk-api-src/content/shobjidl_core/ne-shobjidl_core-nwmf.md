---
UID: NE:shobjidl_core.NWMF
title: NWMF
author: windows-sdk-content
description: Flags used by INewWindowManager::EvaluateNewWindow. These values are factors in the decision of whether to display a pop-up window.
old-location: shell\NWMF.htm
old-project: shell
ms.assetid: b55b60ae-fb56-4525-8113-35c417b28954
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: NWMF, NWMF enumeration [Windows Shell], NWMF_FIRST, NWMF_FORCETAB, NWMF_FORCEWINDOW, NWMF_FROMDIALOGCHILD, NWMF_HTMLDIALOG, NWMF_INACTIVETAB, NWMF_OVERRIDEKEY, NWMF_SHOWHELP, NWMF_SUGGESTTAB, NWMF_SUGGESTWINDOW, NWMF_UNLOADING, NWMF_USERALLOWED, NWMF_USERINITED, NWMF_USERREQUESTED, _shell_NWMF, shell.NWMF, shobjidl_core/NWMF, shobjidl_core/NWMF_FIRST, shobjidl_core/NWMF_FORCETAB, shobjidl_core/NWMF_FORCEWINDOW, shobjidl_core/NWMF_FROMDIALOGCHILD, shobjidl_core/NWMF_HTMLDIALOG, shobjidl_core/NWMF_INACTIVETAB, shobjidl_core/NWMF_OVERRIDEKEY, shobjidl_core/NWMF_SHOWHELP, shobjidl_core/NWMF_SUGGESTTAB, shobjidl_core/NWMF_SUGGESTWINDOW, shobjidl_core/NWMF_UNLOADING, shobjidl_core/NWMF_USERALLOWED, shobjidl_core/NWMF_USERINITED, shobjidl_core/NWMF_USERREQUESTED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NWMF
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shobjidl_core.h
api_name:
-	NWMF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# NWMF enumeration


## -description


Flags used by <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">INewWindowManager::EvaluateNewWindow</a>. These values are factors in the decision of whether to display a pop-up window.


## -enum-fields




### -field NWMF_UNLOADING

The page is unloading. This flag is set in response to the <a href="_inet_IHTMLWindow2_Interface_inet_Onbeforeunload_Property_cpp">onbeforeunload</a> and <a href="_inet_IHTMLWindow2_Interface_inet_Onunload_Property_cpp">onunload</a> events. Some pages load pop-up windows when you leave them, not when you enter. This flag is used to identify those situations.


### -field NWMF_USERINITED


        The call to <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">INewWindowManager::EvaluateNewWindow</a> is the result of a user-initiated action (a mouse click or key press). Use this flag in conjunction with the <a href="https://msdn.microsoft.com/b55b60ae-fb56-4525-8113-35c417b28954">NWMF_FIRST_USERINITED</a> flag to determine whether the call is a direct or indirect result of the user-initiated action.


### -field NWMF_FIRST

When <a href="https://msdn.microsoft.com/b55b60ae-fb56-4525-8113-35c417b28954">NWMF_USERINITED</a> is present, this flag indicates that the call to <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">INewWindowManager::EvaluateNewWindow</a> is the first query that results from this user-initiated action. Always use this flag in conjunction with <a href="https://msdn.microsoft.com/b55b60ae-fb56-4525-8113-35c417b28954">NWMF_USERINITED</a>.


### -field NWMF_OVERRIDEKEY


        The override key (ALT) was pressed. The override key is used to bypass the pop-up manager—allowing all pop-up windows to display—and must be held down at the time that <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">INewWindowManager::EvaluateNewWindow</a> is called. 
            
                

<div class="alert"><b>Note</b>  When <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">INewWindowManager::EvaluateNewWindow</a> is implemented for a <a href="_inet_MLang_1">WebBrowser</a> control host, the implementer can choose to ignore the override key.</div>
<div> </div>

### -field NWMF_SHOWHELP


        The new window attempting to load is the result of a call to the <a href="_inet_showHelp_Method_scr">showHelp</a> method. Help is sometimes displayed in a separate window, and this flag is valuable in those cases.


### -field NWMF_HTMLDIALOG


        The new window is a dialog box that displays HTML content.


### -field NWMF_FROMDIALOGCHILD


        The <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">EvaluateNewWindow</a> method is being called from an HTML dialog. The new window should not show the UI in the parent window.


### -field NWMF_USERREQUESTED

The new windows was definitely requested by the user, either by selecting Open in New Window from a context menu or pressing Shift and clicking a link.
            


### -field NWMF_USERALLOWED

The call to the <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">EvaluateNewWindow</a> method is the result of the user requesting a replay that resulted in a refresh.
            


### -field NWMF_FORCEWINDOW

The new window should be forced to open in a new window rather than a tab.
            


### -field NWMF_FORCETAB

The new window should be forced to open in a new tab.
            


### -field NWMF_SUGGESTWINDOW

The new window should open in a new tab unless <a href="https://msdn.microsoft.com/b55b60ae-fb56-4525-8113-35c417b28954">NWMF_FORCEtab</a> is also present, indicating that user wants the window to open as a window.
            


### -field NWMF_SUGGESTTAB

The new window should open in a new tab unless <a href="https://msdn.microsoft.com/b55b60ae-fb56-4525-8113-35c417b28954">NWMF_FORCEWINDOW</a> is also present, indicating that user wants the window to open as a window.
            


### -field NWMF_INACTIVETAB

The <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">EvaluateNewWindow</a> method is being called from an inactive tab.
            

