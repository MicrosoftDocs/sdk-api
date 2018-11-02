---
UID: NC:winwlx.PWLX_DIALOG_BOX_INDIRECT_PARAM
title: PWLX_DIALOG_BOX_INDIRECT_PARAM
author: windows-sdk-content
description: Called by GINA to initialize dialog box controls and then create a modal dialog box from a dialog box template in memory.
old-location: security\wlxdialogboxindirectparam.htm
tech.root: secauthn
ms.assetid: 98541411-45c7-4c23-95a0-c76022184db3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PWLX_DIALOG_BOX_INDIRECT_PARAM, PWLX_DIALOG_BOX_INDIRECT_PARAM callback, WlxDialogBoxIndirectParam, WlxDialogBoxIndirectParam callback function [Security], _gina_wlxdialogboxindirectparam, security.wlxdialogboxindirectparam, winwlx/WlxDialogBoxIndirectParam
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - winwlx.h
api_name:
 - WlxDialogBoxIndirectParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_DIALOG_BOX_INDIRECT_PARAM callback function


## -description


<p class="CCE_Message">[The WlxDialogBoxIndirectParam function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to initialize dialog box controls and then create a modal dialog box from a dialog box template in memory.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specifies the <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param hInst [in]

Specifies the instance of the module that creates the dialog box.


### -param hDialogTemplate [in]

Specifies the address of a global memory object that contains a dialog box template used to create the dialog box. The template is in the form of a 
<a href="_win32_dlgtemplate_str_cpp">DLGTEMPLATE</a> structure followed by one or more 
<a href="_win32_dlgitemtemplate_str_cpp">DLGITEMTEMPLATE</a> structures. For a full description of these structures, see the Platform SDK.


### -param hwndOwner [in]

Specifies the window that owns the dialog box.


### -param dlgprc [in]

Points to the dialog box procedure. For more information about the dialog box procedure, see the description of the 
<a href="_win32_dialogproc_cpp">DialogProc</a> callback function in the Platform SDK.


### -param dwInitParam [in]

Specifies the value used to initialize the dialog box control. This value is passed to the dialog box in the <i>lParam</i> parameter of the 
<a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a> message.


## -returns



If the function succeeds, the function returns the <i>nResult</i> parameter given in the call to the 
<a href="_win32_enddialog_cpp">EndDialog</a> function used to terminate the dialog box. The following table lists some possible success return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_DLG_INPUT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Input timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_DLG_SAS</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS) event occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_DLG_SCREEN_SAVER_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The screen saver timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_DLG_USER_LOGOFF</b></dt>
</dl>
</td>
<td width="60%">
The user logged off.

</td>
</tr>
</table>
 

If the function fails, the return value is –1.




## -remarks



<b>WlxDialogBoxIndirectParam</b> duplicates the Windows <a href="_win32_dialogboxindirectparam_cpp">DialogBoxIndirectParam</a> function and also allows Winlogon to terminate the dialog box. For more information, see 
<b>DialogBoxIndirectParam</b>.




## -see-also




<a href="_win32_dlgitemtemplate_str_cpp">DLGITEMTEMPLATE</a>



<a href="_win32_dlgtemplate_str_cpp">DLGTEMPLATE</a>



<a href="_win32_dialogboxindirectparam_cpp">DialogBoxIndirectParam</a>



<a href="_win32_dialogproc_cpp">DialogProc</a>



<a href="_win32_enddialog_cpp">EndDialog</a>



<a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

