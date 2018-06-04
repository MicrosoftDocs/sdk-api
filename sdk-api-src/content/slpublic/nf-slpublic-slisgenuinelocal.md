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

# SLIsGenuineLocal function


## -description


Checks whether the specified application is a genuine Windows installation.


## -parameters




### -param pAppId [in]

A pointer to an <b>SLID</b> structure that specifies the application to check.


### -param pGenuineState [out]

A pointer to a value of the <a href="https://msdn.microsoft.com/3be69be1-289c-466a-9271-5309fd1319fe">SL_GENUINE_STATE</a> enumeration that specifies the state of the installation.


### -param pUIOptions [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5e793f09-1d12-4b69-8ba6-6c45421df533">SL_NONGENUINE_UI_OPTIONS</a> structure that specifies a dialog box to display if the installation is not genuine. If the value of this parameter is <b>NULL</b>, no dialog box is displayed.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function checks the <b>Tampered</b> flag of the license associated with the specified application. If the license is not valid, or if the <b>Tampered</b> flag of the license is set, the installation is not considered valid.



