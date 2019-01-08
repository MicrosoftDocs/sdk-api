---
UID: NC:winwlx.PWLX_DIALOG_BOX_INDIRECT
title: PWLX_DIALOG_BOX_INDIRECT
author: windows-sdk-content
description: Called by GINA to create a modal dialog box from a dialog box template in memory.
old-location: security\wlxdialogboxindirect.htm
tech.root: SecAuthN
ms.assetid: adace4e8-659e-4360-985d-d3daafdd3688
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PWLX_DIALOG_BOX_INDIRECT, PWLX_DIALOG_BOX_INDIRECT callback, WlxDialogBoxIndirect, WlxDialogBoxIndirect callback function [Security], _gina_wlxdialogboxindirect, security.wlxdialogboxindirect, winwlx/WlxDialogBoxIndirect
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
 - WlxDialogBoxIndirect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_DIALOG_BOX_INDIRECT callback function


## -description


<p class="CCE_Message">[The WlxDialogBoxIndirect function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to create a modal dialog box from a dialog box template in memory.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Winlogon handle provided to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param hInst [in]

Identifies the instance of the module that creates the dialog box.


### -param hDialogTemplate [in]

Specifies the address of a global memory object that contains a dialog box template used to create the dialog box. The template is in the form of a 
<a href="https://msdn.microsoft.com/en-us/library/ms645394(v=VS.85).aspx">DLGTEMPLATE</a> structure followed by one or more 
<a href="https://msdn.microsoft.com/en-us/library/ms644997(v=VS.85).aspx">DLGITEMTEMPLATE</a> structures. For a full description of these structures, see the Platform SDK.


### -param hwndOwner [in]

Identifies the window that owns the dialog box.


### -param dlgprc [in]

Points to the dialog box procedure. For more information about the dialog box procedure, see 
<a href="https://msdn.microsoft.com/library/ms645469(v=VS.85).aspx">DialogProc</a>.


## -returns



If the <b>WlxDialogBoxIndirect</b> function succeeds, the return value is the <i>nResult</i> parameter given in the call to the 
<a href="https://msdn.microsoft.com/en-us/library/ms645472(v=VS.85).aspx">EndDialog</a> function used to terminate the dialog box. The following table lists some possible success return values.

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



<b>WlxDialogBoxIndirect</b> duplicates the Windows <a href="https://msdn.microsoft.com/en-us/library/ms645457(v=VS.85).aspx">DialogBoxIndirect</a> macro, and also allows Winlogon to terminate the dialog box. For more information, see 
<b>DialogBoxIndirect</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms644997(v=VS.85).aspx">DLGITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645394(v=VS.85).aspx">DLGTEMPLATE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645457(v=VS.85).aspx">DialogBoxIndirect</a>



<a href="https://msdn.microsoft.com/library/ms645469(v=VS.85).aspx">DialogProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645472(v=VS.85).aspx">EndDialog</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

