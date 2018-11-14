---
UID: NS:icm._tagCOLORMATCHSETUPW
title: "_tagCOLORMATCHSETUPW"
author: windows-sdk-content
description: The COLORMATCHSETUP structure contains information that the SetupColorMatching function uses to initialize the ColorManagement dialog box.
old-location: wcs\colormatchsetup.htm
tech.root: WCS
ms.assetid: 920c9ac2-bb77-4805-9345-15611db1aade
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPCOLORMATCHSETUPW, *PCOLORMATCHSETUPW, COLORMATCHSETUP, COLORMATCHSETUP structure [Windows Color System], COLORMATCHSETUPW, _color_COLORMATCHSETUP_str, _tagCOLORMATCHSETUPA, _tagCOLORMATCHSETUPW, icm/COLORMATCHSETUP, wcs.colormatchsetup"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: icm.h
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
 - HeaderDef
api_location:
 - Icm.h
api_name:
 - COLORMATCHSETUP
product: Windows
targetos: Windows
req.typenames: COLORMATCHSETUPW, *PCOLORMATCHSETUPW, *LPCOLORMATCHSETUPW
req.redist: 
---

# _tagCOLORMATCHSETUPW structure


## -description



The <b>COLORMATCHSETUP</b> structure contains information that the <a href="https://msdn.microsoft.com/7d3b6d3f-49f4-46f5-a43b-868e53965d8f">SetupColorMatching</a> function uses to initialize the <b>Color</b><b>Management</b> dialog box. After the user closes the dialog box, <b>SetupColorMatching</b> returns information about the user's selection in this structure.




## -struct-fields




### -field dwSize

Size of the structure. Should be set to <b>sizeof</b> ( <b>COLORMATCHSETUP</b> ).


### -field dwVersion

Version of the <b>COLORMATCHSETUP</b> structure. This should be set to COLOR_MATCH_VERSION.


### -field dwFlags

A set of bit flags used to initialize the dialog box. If set to 0 on entry, all controls assume their default states.

When the dialog box returns, these flags are set to indicate the user's input.

This member can be set using a combination of the following flags.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>CMS_DISABLEICM</td>
<td>If set on entry, this flag indicates that the "Enable Color Management" check box is cleared, disabling all other controls. If set on exit, it means that the user does not wish color management performed.</td>
</tr>
<tr>
<td>CMS_ENABLEPROOFING</td>
<td>If set on entry, this flag indicates that the Proofing controls are to be enabled, and the Proofing check box is checked. If set on exit, it means that the user wishes to perform color management for a different target device than the selected printer.</td>
</tr>
<tr>
<td>CMS_SETRENDERINTENT</td>
<td>If set on entry, this flag indicates that the <b>dwRenderIntent</b> member contains the value to use to initialize the Rendering Intent control. Otherwise, the control defaults to Picture rendering. This flag is set on exit if WCS is enabled.</td>
</tr>
<tr>
<td>CMS_SETPROOFINTENT</td>
<td>Ignored unless CMS_ENABLEPROOFING is also set. If set on entry, and CMS_ENABLEPROOFING is also set, this flag indicates that the <b>dwProofingIntent</b> member is to be used to initialize the Target Rendering Intent control. Otherwise, the control defaults to Picture rendering. This flag is set on exit if proofing is enabled.</td>
</tr>
<tr>
<td>CMS_SETMONITORPROFILE</td>
<td>If set on entry, this flag indicates that the color management profile named in the <b>pMonitorProfile</b> member is to be the initial selection in the monitor profile control. If the specified profile is not associated with the monitor, this flag is ignored, and the default profile for the monitor is used.</td>
</tr>
<tr>
<td>CMS_SETPRINTERPROFILE</td>
<td>If set on entry, this flag indicates that the color management profile named in the <b>pPrinterProfile</b> member is to be the initial selection in the printer profile control. If the specified profile is not associated with the printer, this flag is ignored, and the default profile for the printer is used.</td>
</tr>
<tr>
<td>CMS_SETTARGETPROFILE</td>
<td>If set on entry, this flag indicates that the color profile named in the <b>pTargetProfile</b> member is to be the initial selection in the target profile control. If the specified profile is not installed, this flag is ignored, and the default profile for the printer is used. If the printer has no default profile, then the first profile in alphabetical order will be displayed.</td>
</tr>
<tr>
<td>CMS_USEHOOK</td>
<td>This flag specifies that the <b>lpfnHook</b> member contains the address of a hook procedure, and the <b>lParam</b> member contains a value to be passed to the hook procedure when the WM_INITDIALOG message is sent.</td>
</tr>
<tr>
<td>CMS_MONITOROVERFLOW</td>
<td>This flag is set on exit if color management is to be enabled and the buffer size given in <b>ccMonitorProfile</b> is insufficient for the selected profile name. <b>GetLastError</b> returns ERROR_INSUFFICIENT_BUFFER in such a case.</td>
</tr>
<tr>
<td>CMS_PRINTERROVERFLOW</td>
<td>This flag is set on exit if color management is to be enabled and the buffer size given in <b>ccPrinterProfile</b> is insufficient for the selected profile name. <b>GetLastError</b> returns ERROR_INSUFFICIENT_BUFFER in such a case.</td>
</tr>
<tr>
<td>CMS_TARGETOVERFLOW</td>
<td>This flag is set on exit if proofing is to be enabled and the buffer size given in <b>ccTargetProfile</b> is insufficient for the selected profile name. <b>GetLastError</b> returns ERROR_INSUFFICIENT_BUFFER in such a case.</td>
</tr>
<tr>
<td>CMS_USEAPPLYCALLBACK</td>
<td>If set on entry, this flag indicates that the <b>SetupColorMatching</b> function should call the function <a href="https://msdn.microsoft.com/0f98f6ca-d772-4214-b0aa-f439b214ce4e">ApplyCallbackFunction</a>. The address of the callback function is contained in <i>lpfnApplyCallback</i>.</td>
</tr>
<tr>
<td>CMS_USEDESCRIPTION</td>
<td>If set on entry, this flag instructs the <b>SetupColorMatching</b> function to retrieve the profile description contained in the profile description tags (See ICC Profile Format Specification v3.4). It will insert them into the <b>Monitor Profile</b>, <b>Printer Profile</b>, <b>Emulated Device Profile</b> edit boxes in the <b>Color Management</b> common dialog box.</td>
</tr>
</table>
 


### -field hwndOwner

The window handle to the owner of the dialog box, or <b>NULL</b> if the dialog box has no owner.


### -field pSourceName

Pointer to an application-specified string which describes the source profile of the item for which color management is to be performed. If this is <b>NULL</b>, the Image Source control displays the name of the Windows default color profile.


### -field pDisplayName

Points to a string naming the monitor to be used for color management. If this is not the name of a valid monitor, the first enumerated monitor is used.


### -field pPrinterName

Points to a string naming the printer on which the image is to be rendered. If this is not a valid printer name, the default printer is used and named in the dialog.


### -field dwRenderIntent

The type of color management desired. Valid values are:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -field dwProofingIntent

The type of color management desired for the proofed image. Valid values are:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -field pMonitorProfile

Pointer to a buffer in which to place the name of the user-selected monitor profile. If the CMS_SETMONITORPROFILE flag is used, this flag can also be used to select a profile other than the monitor default when the dialog is first displayed.


### -field ccMonitorProfile

The size of the buffer pointed to by the <b>pMonitorProfile</b> member, in characters. If the buffer is not large enough to hold the selected name, the name is truncated to this size, and ERROR_INSUFFICIENT_BUFFER is returned. A buffer of MAX_PATH size always works.


### -field pPrinterProfile

Points to a buffer in which to place the name of the user-selected printer profile. If the CMS_SETPRINTERPROFILE flag is used, this flag can also be used to select a profile other than the printer default when the dialog is first displayed.


### -field ccPrinterProfile

The size of the buffer pointed to by the <b>pPrinterProfile</b> member, in characters. If the buffer is not large enough to hold the selected name, the name is truncated to this size, and ERROR_INSUFFICIENT_BUFFER is returned. A buffer of MAX_PATH size always works.


### -field pTargetProfile

Points to a buffer in which to place the name of the user-selected target profile for proofing. If the CMS_SETTARGETPROFILE flag is used, this flag can also be used to select a profile other than the printer default when the dialog is first displayed.


### -field ccTargetProfile

The size of the buffer pointed to by the <b>pTargetProfile</b> member, in characters. If the buffer is not large enough to hold the selected name, the name is truncated to this size, and ERROR_INSUFFICIENT_BUFFER is returned. A buffer of MAX_PATH size always works.


### -field lpfnHook

If the CMS_USEHOOK flag is set, this member is the address of a dialog procedure (see <a href="_win32_dialogproc">DialogProc</a> ) that can filter or handle messages for the dialog. The hook procedure receives no messages issued before WM_INITDIALOG. It is called on the WM_INITDIALOG message after the system-provided dialog procedure has processed the message. On all other messages, the hook procedure receives the message before the system-provided procedure. If the hook procedure returns <b>TRUE</b> to these messages, the system-provided procedure is not called.

The hook procedure may call the <a href="_win32_enddialog">EndDialog</a> function.


### -field lParam

If the CMS_USEHOOK flag is set, this member is passed to the application-provided hook procedure as the <i>lParam</i> parameter when the WM_INITDIALOG message is processed.


### -field lpfnApplyCallback

Contains a pointer to a callback function that is invoked when the <b>Apply</b> button of the Color Management dialog box is selected. If no callback function is provided, this member should be set to <b>NULL</b>. See <a href="https://msdn.microsoft.com/0f98f6ca-d772-4214-b0aa-f439b214ce4e">ApplyCallbackFunction</a>.


### -field lParamApplyCallback

Contains a value that will be passed to the function <b>ApplyCallbackFunction</b> through its <i>lParam</i> parameter. The meaning and content of the value is specified by the application.


## -see-also




<a href="what_s_new_in_version_1_0_of_wcs.htm">A Common Dialog for Color Management</a>



<a href="_win32_dialogproc">DialogProc</a>



<a href="_win32_enddialog">EndDialog</a>
 

 

