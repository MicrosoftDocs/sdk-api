---
UID: NF:oleacc.IAccessible.get_accHelpTopic
title: IAccessible::get_accHelpTopic
author: windows-sdk-content
description: The IAccessible::get_accHelpTopic method retrieves the full path of the WinHelp file that is associated with the specified object; it also retrieves the identifier of the appropriate topic within that file.
old-location: winauto\iaccessible_iaccessible__get_acchelptopic.htm
tech.root: WinAuto
ms.assetid: a8f4ae56-6bd9-4615-a87d-a4de2f7632b1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accHelpTopic method, IAccessible.get_accHelpTopic, IAccessible::get_accHelpTopic, _msaa_IAccessible_get_accHelpTopic, get_accHelpTopic, get_accHelpTopic method [Windows Accessibility], get_accHelpTopic method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_acchelptopic, oleacc/IAccessible::get_accHelpTopic, winauto.iaccessible_iaccessible__get_acchelptopic
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessible.get_accHelpTopic
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# IAccessible::get_accHelpTopic


## -description


The <b>IAccessible::get_accHelpTopic</b> method retrieves the full path of the WinHelp file that is associated with the specified object; it also retrieves the identifier of the appropriate topic within that file. Not all objects support this property. This property is rarely supported or used by  applications
<div class="alert"><b>Note</b>  <b>IAccessible::get_accHelpTopic</b> is deprecated and should not be used.</div><div> </div>

## -parameters




### -param pszHelpFile [out]

Type: <b>BSTR*</b>

Address of a <b>BSTR</b> that receives the full path of the WinHelp file that is associated with the specified object.


### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved Help topic belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain a Help topic for the object) or a child ID (to obtain a Help topic for one of the object's child elements). For more information about initializing the <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


### -param pidTopic

Type: <b>long*</b>

[out, retval] Address of a variable that identifies the Help file topic associated with the specified object. This value is used as the context identifier of the desired topic that passes to the <a href="https://go.microsoft.com/fwlink/p/?linkid=177910">WinHelp</a> function. When calling <a href="https://go.microsoft.com/fwlink/p/?linkid=177910">WinHelp</a> to display the topic, set the <i>uCommand</i> parameter to HELP_CONTEXT, cast the value pointed to by <i>pidTopic</i> to a <b>DWORD</b>, and pass it as the <i>dwData</i> parameter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="https://msdn.microsoft.com/0def0349-178b-4be5-aa1d-6602dc015981">Checking IAccessible Return Values</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No Help information is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The object does not support this property.

</td>
</tr>
</table>
 




## -remarks



Getting information from a Help file might be time and memory intensive.

<b>Note to server developers:  </b>This property provides access to a Help topic in WinHelp, whereas <a href="https://msdn.microsoft.com/ef541ef9-ae9f-4a8c-8dd1-f221eddb55c7">IAccessible::get_accHelp</a> returns a string. Objects are not required to support both <b>IAccessible::get_accHelp</b> and <b>IAccessible::get_accHelpTopic</b>, but they must support at least one. If they can easily return a string, they must support <b>IAccessible::get_accHelp</b>; otherwise they must support <b>IAccessible::get_accHelpTopic</b>. If both are supported, <b>IAccessible::get_accHelpTopic</b> provides more detailed information.




## -see-also




<a href="https://msdn.microsoft.com/07681d62-c7b4-439f-b43a-57f430914d4a">HelpTopic Property</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/ef541ef9-ae9f-4a8c-8dd1-f221eddb55c7">IAccessible::get_accHelp</a>
 

 

