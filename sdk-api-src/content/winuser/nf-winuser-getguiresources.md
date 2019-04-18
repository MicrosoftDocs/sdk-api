---
UID: NF:winuser.GetGuiResources
title: GetGuiResources function (winuser.h)
author: windows-sdk-content
description: Retrieves the count of handles to graphical user interface (GUI) objects in use by the specified process.
old-location: base\getguiresources.htm
tech.root: ProcThread
ms.assetid: 55fbb7e8-79b4-4011-b522-25ea5a928b86
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GR_GDIOBJECTS, GR_GDIOBJECTS_PEAK, GR_USEROBJECTS, GR_USEROBJECTS_PEAK, GetGuiResources, GetGuiResources function, _win32_getguiresources, base.getguiresources, winuser/GetGuiResources
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetGuiResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetGuiResources function


## -description


Retrieves the count of handles to graphical user interface (GUI) objects in use by the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param uiFlags [in]

The GUI object type. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GR_GDIOBJECTS"></a><a id="gr_gdiobjects"></a><dl>
<dt><b>GR_GDIOBJECTS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Return the count of GDI objects.

</td>
</tr>
<tr>
<td width="40%"><a id="GR_GDIOBJECTS_PEAK"></a><a id="gr_gdiobjects_peak"></a><dl>
<dt><b>GR_GDIOBJECTS_PEAK</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Return the peak count of GDI objects.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows 7 and Windows Server 2008 R2.

</td>
</tr>
<tr>
<td width="40%"><a id="GR_USEROBJECTS"></a><a id="gr_userobjects"></a><dl>
<dt><b>GR_USEROBJECTS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Return the count of USER objects.

</td>
</tr>
<tr>
<td width="40%"><a id="GR_USEROBJECTS_PEAK"></a><a id="gr_userobjects_peak"></a><dl>
<dt><b>GR_USEROBJECTS_PEAK</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Return the peak count of USER objects.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows 7 and Windows Server 2008 R2.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is the count of handles to GUI objects in use by the process. If no GUI objects are in use, the return value is zero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A process without a graphical user interface does not use GUI resources, therefore, 
<b>GetGuiResources</b> will return zero.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

