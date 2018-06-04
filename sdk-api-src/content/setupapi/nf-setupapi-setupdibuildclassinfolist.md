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

# SetupDiBuildClassInfoList function


## -description


The <b>SetupDiBuildClassInfoList</b> function returns a list of setup class GUIDs that identify the classes that are installed on a local computer.


## -parameters




### -param Flags [in]

Flags used to control exclusion of classes from the list. If no flags are specified, all setup classes are included in the list. Can be a combination of the following values:





#### DIBCI_NOINSTALLCLASS

Exclude a class if it has the <b>NoInstallClass</b> value entry in its registry key.



#### DIBCI_NODISPLAYCLASS

Exclude a class if it has the <b>NoDisplayClass</b> value entry in its registry key.


### -param ClassGuidList [out, optional]

A pointer to a GUID-typed array that receives a list of setup class GUIDs. This pointer is optional and can be <b>NULL</b>.


### -param ClassGuidListSize [in]

The number of GUIDs in the array that is pointed to by the <i>ClassGuildList</i> parameter. If <i>ClassGuidList</i> is <b>NULL</b>, <i>ClassGuidSize</i> must be zero.


### -param RequiredSize [out]

A pointer to a DWORD-typed variable that receives the number of GUIDs that are returned (if the number is less than or equal to the size, in GUIDs, of the array that is pointed to by the <i>ClassGuidList</i> parameter). 

If this number is greater than the size of the <i>ClassGuidList</i> array, it indicates how large the <i>ClassGuidList</i> array must be in order to contain all the class GUIDs.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



To retrieve the number of classes that are installed on a local computer, call <b>SetupDiBuildClassInfoList</b> with <i>ClassGuidList</i> set to <b>NULL</b> and <i>ClassGuidSize</i> set to zero. In response to such a call, the function returns the number of classes in <b>*</b><i>RequiredSize</i>.

<b>SetupDiBuildClassInfoList</b> does not return a class GUID for a class if the <b>NoUseClass</b> value entry exists in the registry key of the class.

To retrieve the list of setup class GUIDs installed on a remote system use <a href="https://msdn.microsoft.com/library/windows/hardware/ff550911">SetupDiBuildClassInfoListEx</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550911">SetupDiBuildClassInfoListEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551053">SetupDiGetClassDescription</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552010">SetupDiGetINFClass</a>
 

 

