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

# _SERVICE_FAILURE_ACTIONSA structure


## -description


Represents the action the service controller should take on each failure of a service. A service is considered failed when it terminates without reporting a status of <b>SERVICE_STOPPED</b> to the service controller.

To configure additional circumstances under which the failure actions are to be executed, see <a href="https://msdn.microsoft.com/49736b26-9565-4d56-abcd-1585b692ff12">SERVICE_FAILURE_ACTIONS_FLAG</a>.


## -struct-fields




### -field dwResetPeriod

The time after which to reset the failure count to zero if there are no failures, in seconds. Specify <b>INFINITE</b> to indicate that this value should never be reset.


### -field lpRebootMsg

The message to be broadcast to server users before rebooting in response to the <b>SC_ACTION_REBOOT</b> service controller action. 




If this value is <b>NULL</b>, the reboot message is unchanged. If the value is an empty string (""), the reboot message is deleted and no message is broadcast.

This member can specify a localized string using the following format:

@[<i>path</i>\]<i>dllname</i>,-<i>strID</i>

The string with identifier <i>strID</i> is loaded from <i>dllname</i>; the <i>path</i> is optional. For more information, see <a href="https://msdn.microsoft.com/76ffc77f-a1bc-4e01-858f-4a76563a2bbc">RegLoadMUIString</a>.

<b>Windows Server 2003 and Windows XP:  </b>Localized strings are not supported until Windows Vista.


### -field lpCommand

The command line of the process for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function to execute in response to the <b>SC_ACTION_RUN_COMMAND</b> service controller action. This process runs under the same account as the service. 




If this value is <b>NULL</b>, the command is unchanged. If the value is an empty string (""), the command is deleted and no program is run when the service fails.


### -field cActions

The number of elements in the <b>lpsaActions</b> array. 




If this value is 0, but <b>lpsaActions</b> is not NULL, the reset period and array of failure actions are deleted.


### -field cActions.range

 


### -field cActions.range.0

 


### -field cActions.range.1024

 


### -field lpsaActions

A pointer to an array of 
<a href="https://msdn.microsoft.com/e2c355a6-affe-46bf-a3e6-f8c420422d46">SC_ACTION</a> structures. 




If this value is NULL, the <b>cActions</b> and <b>dwResetPeriod</b> members are ignored.


### -field lpsaActions.size_is

 


### -field lpsaActions.size_is.cActions

 




## -remarks



The service control manager counts the number of times each service has failed since the system booted. The count is reset to 0 if the service has not failed for <b>dwResetPeriod</b> seconds. When the service fails for the <i>N</i>th time, the service controller performs the action specified in element [<i>N</i>-1] of the <b>lpsaActions</b> array. If <i>N</i> is greater than <i>cActions</i>, the service controller repeats the last action in the array.




## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>



<a href="https://msdn.microsoft.com/e2c355a6-affe-46bf-a3e6-f8c420422d46">SC_ACTION</a>



<a href="https://msdn.microsoft.com/49736b26-9565-4d56-abcd-1585b692ff12">SERVICE_FAILURE_ACTIONS_FLAG</a>
 

 

