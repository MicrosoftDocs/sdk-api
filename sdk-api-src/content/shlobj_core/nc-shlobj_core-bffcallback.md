---
UID: NC:shlobj_core.BFFCALLBACK
title: BFFCALLBACK (shlobj_core.h)
description: Receives event notifications from the Active Directory Domain Services container browser dialog box.
helpviewer_keywords: ["BFFCALLBACK","BFFCALLBACK callback function [Active Directory]","BFFCallBack","BFFCallBack callback","BFFCallBack callback function [Active Directory]","BFFM_ENABLEOK","BFFM_INITIALIZED","BFFM_SELCHANGED","BFFM_SETSELECTION","DSBM_CHANGEIMAGESTATE","DSBM_CONTEXTMENU","DSBM_HELP","DSBM_QUERYINSERT","_glines_bffcallback","ad.bffcallback","shlobj_core/BFFCallBack"]
old-location: ad\bffcallback.htm
tech.root: ad
ms.assetid: 91cfef29-3e0a-4dd0-be1a-215827c23143
ms.date: 12/05/2018
ms.keywords: BFFCALLBACK, BFFCALLBACK callback function [Active Directory], BFFCallBack, BFFCallBack callback, BFFCallBack callback function [Active Directory], BFFM_ENABLEOK, BFFM_INITIALIZED, BFFM_SELCHANGED, BFFM_SETSELECTION, DSBM_CHANGEIMAGESTATE, DSBM_CONTEXTMENU, DSBM_HELP, DSBM_QUERYINSERT, _glines_bffcallback, ad.bffcallback, shlobj_core/BFFCallBack
req.header: shlobj_core.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BFFCALLBACK
 - shlobj_core/BFFCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - shlobj_core.h
api_name:
 - BFFCALLBACK
---

# BFFCALLBACK callback function


## -description

The <b>BFFCallBack</b> function is an application-defined callback function that receives event notifications from the Active Directory Domain Services container browser dialog box. A pointer to this function is supplied to the container browser dialog box in the <b>pfnCallback</b> member of the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsbrowseinfoa">DSBROWSEINFO</a> structure when the <a href="/windows/desktop/api/dsclient/nf-dsclient-dsbrowseforcontainera">DsBrowseForContainer</a> function is called. <b>BFFCallBack</b> is a placeholder for the application-defined function name.

## -parameters

### -param hwnd [in]

Contains the window handle of the browse dialog box. This handle is used to send messages to the browse dialog box using the <a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a> function.


The container browser dialog box handles the following messages.





#### BFFM_ENABLEOK

This message enables or disables the <b>OK</b> command button in the dialog box.

The <i>wParam</i> of this message contains a Boolean value that, if zero, disables the <b>OK</b> command button. If the <i>wParam</i> is nonzero, the <b>OK</b> command button is enabled. By default, the <b>OK</b> command button is enabled.

The return value for this message is not used.



#### BFFM_SETSELECTION

This message selects an item in the dialog box.

The <i>lParam</i> of this message is a pointer to a <b>TCHAR</b> string that contains the ADsPath of the item to be selected. Even though there are ANSI and Unicode versions of this message, both versions take a pointer to a Unicode string.

The return value for this message is not used.

### -param uMsg [in]

Specifies one of the following browse messages.



#### BFFM_INITIALIZED

This notification is sent after the dialog box is initialized.

<i>lParam</i> is not used.

The return value from this notification is ignored.



#### BFFM_SELCHANGED

This notification is sent after the selection in the dialog box is changed.

<i>lParam</i> is a pointer to a Unicode string that contains the ADsPath of the newly selected item.

The return value from this notification is ignored.



#### DSBM_CHANGEIMAGESTATE

Reserved.



#### DSBM_CONTEXTMENU

This notification is sent when the dialog box receives a <a href="/windows/desktop/menurc/wm-contextmenu">WM_CONTEXTMENU</a> message.

<i>lParam</i> is the <i>wParam</i> value passed with the <a href="/windows/desktop/menurc/wm-contextmenu">WM_CONTEXTMENU</a> message.

The return value from this notification is ignored.



#### DSBM_HELP

This notification is sent when the dialog box receives a <a href="/windows/desktop/shell/wm-help">WM_HELP</a> message.

<i>lParam</i> is the <i>lParam</i> value passed with the <a href="/windows/desktop/shell/wm-help">WM_HELP</a> message.

The return value from this notification is ignored.



#### DSBM_QUERYINSERT

This notification is sent prior to each container object being inserted into the tree. The application can use this notification to modify the contents of the dialog box.

<i>lParam</i> is a pointer to a <a href="/windows/desktop/api/dsclient/ns-dsclient-dsbitema">DSBITEM</a> structure that contains data about the item inserted. Some members of this structure, such as <b>szDisplayName</b>, can be modified during this notification to change the way items are displayed.

Return a nonzero value from this notification if data  in the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsbitema">DSBITEM</a> structure changes. Return zero if the time should be inserted unchanged.

<div class="alert"><b>Note</b>  Only the Unicode version of this message, <b>DSBM_QUERYINSERTW</b>, is supported. <b>DSBM_QUERYINSERTA</b> is not supported.</div>
<div> </div>

### -param lParam [in]

The value and meaning of this parameter is determined by the notification received. For more information, see the notification message descriptions under the <i>uMsg</i> parameter.

### -param lpData [in]

Contains a pointer to the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsbrowseinfoa">DSBROWSEINFO</a> structure passed to the <a href="/windows/desktop/api/dsclient/nf-dsclient-dsbrowseforcontainera">DsBrowseForContainer</a> function. This is true for all notification messages.

## -remarks

The <b>DSBM_*</b> message values are defined in Dsclient.h.

## -see-also

<a href="/windows/desktop/api/dsclient/ns-dsclient-dsbitema">DSBITEM</a>



<a href="/windows/desktop/api/dsclient/ns-dsclient-dsbrowseinfoa">DSBROWSEINFO</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-dsbrowseforcontainera">DsBrowseForContainer</a>



<a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a>



<a href="/windows/desktop/menurc/wm-contextmenu">WM_CONTEXTMENU</a>



<a href="/windows/desktop/shell/wm-help">WM_HELP</a>