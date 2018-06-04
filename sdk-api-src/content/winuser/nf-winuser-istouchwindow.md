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

# IsTouchWindow function


## -description


Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.


## -parameters




### -param hwnd

TBD


### -param pulFlags [out, optional]

The address of the <b>ULONG</b> variable to receive the modifier flags for the specified window's touch capability.


#### - hWnd [in]

The handle of the window. The function fails with <b>ERROR_ACCESS_DENIED</b> if the calling thread is not on the same desktop as the specified window.


## -returns



Returns <b>TRUE</b> if the window supports Windows Touch; returns <b>FALSE</b> if the window does not support Windows Touch.




## -remarks




		The following table lists the values for the <i>pulFlags</i> output parameter.
		

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td><b>TWF_FINETOUCH</b></td>
<td>Specifies that <i>hWnd</i> prefers noncoalesced touch input.</td>
</tr>
<tr>
<td><b>TWF_WANTPALM</b></td>
<td>

                       Clearing this flag disables palm rejection which reduces delays for getting <a href="https://msdn.microsoft.com/5dee8bab-34fa-4dd9-a65b-35883757ec80">WM_TOUCH</a> messages. 
						     This is useful if you want as quick of a response as possible when a user touches your application.
						  

Setting this flag enables palm detection and will prevent some <a href="https://msdn.microsoft.com/5dee8bab-34fa-4dd9-a65b-35883757ec80">WM_TOUCH</a> messages from being sent 
						     to your application.  This is useful if you do not want to receive <b>WM_TOUCH</b> messages that are from palm contact.
                    

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

