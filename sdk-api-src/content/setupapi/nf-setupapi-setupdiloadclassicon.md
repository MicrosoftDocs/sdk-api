---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetupDiLoadClassIcon function


## -description


The <b>SetupDiLoadClassIcon</b> function loads both the large and mini-icon for the specified class.


## -parameters




### -param ClassGuid [in]

A pointer to the GUID of the class for which the icon(s) should be loaded.


### -param LargeIcon [out, optional]

A pointer to an icon handle that receives the handle value for the loaded large icon for the specified class. This pointer is optional and can be <b>NULL</b>. If the pointer is <b>NULL</b>, the large icon is not loaded. 


### -param MiniIconIndex [out, optional]

A pointer to an INT-typed variable that receives the index of the mini-icon for the specified class. The mini-icon is stored in the device installer's mini-icon cache. The pointer is optional and can be <b>NULL</b>. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The icons of the class are either predefined and loaded from the device installer's internal cache, or they are loaded directly from the class installer's executable. This function queries the registry value <b>ICON</b> in the specified class's section. If the <b>ICON</b> value is specified, it indicates which mini-icon to load. 

If the <b>ICON</b> value is negative, the absolute value represents a predefined icon in the class's registry. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff551005">SetupDiDrawMiniIcon</a> for a list of the predefined mini-icons. 

If the <b>ICON</b> value is positive, it represents an icon in the class installer's executable image that will be extracted. The value 1 is reserved. This function also uses the <b>INSTALLER32</b> registry value and then the <b>ENUMPROPPAGES32</b> registry value to determine which executable image to extract the icons from. For more information about these registry values, see <a href="devinst.inf_classinstall32_section">INF ClassInstall32 Section</a>.

When a caller is finished using the icon, the caller must call <b>DestroyIcon</b> (which is described in the Microsoft Windows SDK documentation).

If the <i>LargeIcon </i>parameter is specified, but the <i>ClassGuid</i> parameter does not supply a valid class GUID or the <b>Icon</b> registry value of the class is not valid, <b>SetupDiLoadClassIcon</b> loads the default large icon, returns the handle for the large icon, and, if the <i>MiniIconIndex</i> parameter is specified, returns the index of the default mini-icon.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551005">SetupDiDrawMiniIcon</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551047">SetupDiGetClassBitmapIndex</a>
 

 

