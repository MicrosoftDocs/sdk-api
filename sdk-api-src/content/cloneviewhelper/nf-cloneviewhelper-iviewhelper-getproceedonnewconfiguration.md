---
UID: NF:cloneviewhelper.IViewHelper.GetProceedOnNewConfiguration
title: IViewHelper::GetProceedOnNewConfiguration (cloneviewhelper.h)
description: The GetProceedOnNewConfiguration method allows the user-mode display driver to suppress the TMM user interface and display changing actions on a new, two-monitor configuration.
helpviewer_keywords: ["GetProceedOnNewConfiguration","GetProceedOnNewConfiguration method [Display Devices]","GetProceedOnNewConfiguration method [Display Devices]","IViewHelper interface","IViewHelper interface [Display Devices]","GetProceedOnNewConfiguration method","IViewHelper.GetProceedOnNewConfiguration","IViewHelper::GetProceedOnNewConfiguration","TMM_Ref_3cc57f4b-1882-4f95-955c-23b6e8635a98.xml","cloneviewhelper/IViewHelper::GetProceedOnNewConfiguration","display.iviewhelper_getproceedonnewconfiguration"]
old-location: display\iviewhelper_getproceedonnewconfiguration.htm
tech.root: display
ms.assetid: 223fc545-0fe8-4907-870a-7c0e4ec2f2e8
ms.date: 12/05/2018
ms.keywords: GetProceedOnNewConfiguration, GetProceedOnNewConfiguration method [Display Devices], GetProceedOnNewConfiguration method [Display Devices],IViewHelper interface, IViewHelper interface [Display Devices],GetProceedOnNewConfiguration method, IViewHelper.GetProceedOnNewConfiguration, IViewHelper::GetProceedOnNewConfiguration, TMM_Ref_3cc57f4b-1882-4f95-955c-23b6e8635a98.xml, cloneviewhelper/IViewHelper::GetProceedOnNewConfiguration, display.iviewhelper_getproceedonnewconfiguration
req.header: cloneviewhelper.h
req.include-header: Cloneviewhelper.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Windows 7
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
 - IViewHelper::GetProceedOnNewConfiguration
 - cloneviewhelper/IViewHelper::GetProceedOnNewConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Cloneviewhelper.h
api_name:
 - IViewHelper.GetProceedOnNewConfiguration
---

# IViewHelper::GetProceedOnNewConfiguration


## -description

The <b>GetProceedOnNewConfiguration</b> method allows the user-mode display driver to suppress the TMM user interface and display changing actions on a new, two-monitor configuration. This is only the case when a user presses a keyboard shortcut to switch views (such as, FN key combinations like FN, F5) and causes a Hot Plug Detection (HPD) event to occur.



## -returns

The <b>GetProceedOnNewConfiguration</b> method returns one of the following values: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
The TMM user interface can appear.

TMM proceeds with its operations, defaulting to clone view if the current display configuration is in single view. TMM will also open a dialog. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE </b></dt>
</dl>
</td>
<td width="60%">
Both TMM actions and user interface should be suppressed.

TMM will not actively change any display settings and will not show a user interface. The only conditions under which returning S_FALSE are allowed are:

<ul>
<li>
The state change for displays was caused by a user pressing a keyboard shortcut (that is, Fn key combinations). For example, if the user presses a keyboard shortcut to switch views, the  user-mode display driver might have its own user interface to present to the user. In this situation, if the user-mode display driver must suppress TMM actions, this return code can be used to inform TMM. 

</li>
<li>
The state change for displays was caused by user input from the user-mode display driver's user interface. For example, if the user opens a program that was created by the hardware vendor to manually change the connected and active state, an HPD might be generated. In this situation, this return code will prevent TMM from taking action and conflicting with the user's manual input. The driver will then handle the display change. 

</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_INIT </b></dt>
</dl>
</td>
<td width="60%">
Only TMM actions are suppressed. However, TMM user interface is shown.

TMM will not actively change any display settings but can show its user interface. The user-mode display driver has the opportunity to set predefined configurations. However, TMM user interface can still be shown, which allows users to customize the display settings if they do not like the default. 

</td>
</tr>
</table>

## -remarks

<b>GetProceedOnNewConfiguration</b> is called only when an HPD event occurs and TMM encounters a new configuration (that is, a configuration for which TMM does not yet have a profile).

