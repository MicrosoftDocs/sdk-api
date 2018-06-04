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

# SetupDiBuildClassInfoListExA function


## -description


The <b>SetupDiBuildClassInfoListEx</b> function returns a list of setup class GUIDs that includes every class installed on the local system or a remote system.


## -parameters




### -param Flags [in]

Flags used to control exclusion of classes from the list. If no flags are specified, all setup classes are included in the list. Can be a combination of the following values:





#### DIBCI_NOINSTALLCLASS

Exclude a class if it has the <b>NoInstallClass</b> value entry in its registry key.



#### DIBCI_NODISPLAYCLASS

Exclude a class if it has the <b>NoDisplayClass</b> value entry in its registry key.


### -param ClassGuidList [out, optional]

A pointer to a buffer that receives a list of setup class GUIDs.


### -param ClassGuidListSize [in]

Supplies the number of GUIDs in the <i>ClassGuildList</i> array.


### -param RequiredSize [out]

A pointer to a variable that receives the number of GUIDs returned. If this number is greater than the size of the <i>ClassGuidList</i>, the number indicates how large the <i>ClassGuidList</i> array must be in order to contain the list.


### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote computer from which to retrieve installed setup classes. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, this function builds a list of classes installed on the local computer.


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550909">SetupDiBuildClassInfoList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551058">SetupDiGetClassDescriptionEx</a>
 

 

