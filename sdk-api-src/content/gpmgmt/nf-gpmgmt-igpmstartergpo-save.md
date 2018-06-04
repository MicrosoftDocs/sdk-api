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

# IGPMStarterGPO::Save


## -description


Saves all Starter GPO settings into a single CAB file.    Optionally the user may specify to save a custom Starter GPO as a system Starter GPO.


## -parameters




### -param bstrSaveFile [in]

Name of the file to which the Starter GPO should be saved.  Use null-terminated string.


### -param bOverwrite [in]

Boolean value that determines whether the file  should be  overwritten, if it exists.


### -param bSaveAsSystem [in]

Boolean value that specifies whether to convert the Starter GPO into a system template as part of the save.  By default, the value is <b>VARIANT_FALSE</b>, save as a system Starter GPO.  This option must be VARIANT_FALSE if the Starter GPO being saved is a system Starter GPO; entering VARIANT_TRUE for a system Starter GPO will return an invalid argument error.


### -param bstrLanguage [in, optional]

Specifies the MUI language code all the language specific strings of the custom Starter GPO will be exported during the save.  The custom Starter GPO strings are converted into MUI resources without performing any language checks on the strings.  If bSaveAsSystem is VARIANT_FALSE this parameter is ignored.  If this parameter is <b>NULL</b>, the user's current language code is used.


### -param bstrAuthor [in, optional]

Specifies the Author property of the new system Starter GPO.  If bSaveAsSystem is VARIANT_FALSE this parameter is ignored.


### -param bstrProduct [in, optional]

Specifies the Product property of the new system Starter GPO.  If bSaveAsSystem is VARIANT_FALSE this parameter is ignored


### -param bstrUniqueID [in, optional]

Specifies the ID property of the new system Starter GPO.  If the parameter is <b>NULL</b> a new unique ID will be generated.  If bSaveAsSystem is VARIANT_FALSE this parameter is ignored.


### -param bstrVersion [in, optional]

Specifies the Starter GPO version of the new system Starter GPO.  The format of the string must be 4 digits-dot-5 digits.  If the value is <b>NULL</b> the version is set to 1.0.  If bSaveAsSystem is VARIANT_FALSE this parameter is ignored


### -param pvarGPMProgress [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the copy operation. If not <b>NULL</b>, the call to <a href="https://msdn.microsoft.com/d5daa512-547f-4b2d-85b3-0f6e9244acb2">GenerateReport</a> is handled asynchronously and <i>pvarGPMCancel</i> receives a pointer to an <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface.   If this parameter is <b>NULL</b> the call to <b>GenerateReport</b> is handled synchronously. The <i>pvarGPMProgress</i> parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.


### -param pvarGPMCancel [out, optional]

Receives a pointer to an <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a>. The Result property contains a string representing the GUID of the saved Starter GPO.  If bSaveAsSystem is <b>VARIANT_TRUE</b>, the Starter GPO will be saved with a new GUID as specified by bstrUniqueID. The Status property contains a reference to an <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a>
 

 

