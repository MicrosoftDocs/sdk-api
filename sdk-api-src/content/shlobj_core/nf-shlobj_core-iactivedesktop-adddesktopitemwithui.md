---
UID: NF:shlobj_core.IActiveDesktop.AddDesktopItemWithUI
title: IActiveDesktop::AddDesktopItemWithUI
author: windows-sdk-content
description: Adds a desktop item to the Active Desktop after displaying user interfaces that confirm the addition of the desktop item, verifying security zone permissions, and asking if the user wants to create a subscription.
old-location: lwef\iactivedesktop_adddesktopitemwithui_method.htm
tech.root: lwef
ms.assetid: ac582bd7-9fd1-4134-a866-69319ef3d96e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddDesktopItemWithUI, AddDesktopItemWithUI method [Legacy Windows Environment Features], AddDesktopItemWithUI method [Legacy Windows Environment Features],IActiveDesktop interface, DTI_ADDUI_DEFAULT, DTI_ADDUI_DISPSUBWIZARD, DTI_ADDUI_POSITIONITEM, IActiveDesktop interface [Legacy Windows Environment Features],AddDesktopItemWithUI method, IActiveDesktop.AddDesktopItemWithUI, IActiveDesktop::AddDesktopItemWithUI, _win32_IActiveDesktop_AddDesktopItemWithUI_Method, lwef.iactivedesktop_adddesktopitemwithui_method, shell.iactivedesktop_adddesktopitemwithui_method, shlobj_core/IActiveDesktop::AddDesktopItemWithUI
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktop.AddDesktopItemWithUI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::AddDesktopItemWithUI


## -description


Adds a desktop item to the Active Desktop after  displaying user interfaces that confirm the addition of the desktop item, verifying security zone permissions, and asking if the user wants to create a subscription.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the parent window. If <b>NULL</b>, the desktop item is added without displaying any user interface, in accordance with the corresponding security zone permissions. For more information, see <a href="ie.URL_Security_Zones_Overview_9kxc">About URL Security Zones</a>.


### -param pcomp [in]

Type: <b>LPCOMPONENT</b>

Address of the <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a> structure containing the details of the desktop item to be added. 


### -param dwReserved

Type: <b>DWORD</b>

Unsigned long integer value that contains the flags that control how the desktop item is added. Can be one of the following values. 



#### DTI_ADDUI_DEFAULT

Do default action. Identical to using zero.



#### DTI_ADDUI_DISPSUBWIZARD

Activate the subscription wizard to allow the user to subscribe to this desktop item.



#### DTI_ADDUI_POSITIONITEM

Instruct the system to look at the <a href="https://msdn.microsoft.com/622bdf51-d605-4eb9-a692-09be028bbff8">COMPPOS</a> structure passed to the <b>cpPos</b> member of the <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a> structure to ensure that the values are within reasonable limits. This value was added for Internet Explorer 5.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to add the desktop item, or an instance of the desktop item already exists on the Active Desktop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVAILDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
If the <b>ADDURL_SILENT</b> flag has been set, the desktop item has either been added successfully or it already exists on the Active Desktop. Otherwise, the desktop item has been added successfully. 

</td>
</tr>
</table>
 




## -remarks



This method creates a second instance of the <a href="https://msdn.microsoft.com/68d72b0f-f5e9-4fff-bb13-4c60d1dd7009">Active Desktop</a> to add the desktop item, so the desktop item does not appear in the current instance. The application must call the <a href="_com_iunknown_release">IUnknown::Release</a> method on this <a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a> interface and then use the <a href="http://msdn.microsoft.com/en-us/library/ms686615(VS.85).aspx">CoCreateInstance</a> function to retrieve the Active Desktop object with the newly added component.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>



<a href="https://msdn.microsoft.com/68d72b0f-f5e9-4fff-bb13-4c60d1dd7009">Using the Active Desktop Object</a>
 

 

