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

# IGPMBackupDirEx::SearchBackups


## -description


Executes a search for  a <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object or an <b>IGPMStarterGPOBackup</b> interface according to the specified criteria, and returns a 
<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">GPMBackupCollection</a> or <b>GPMStarterGPOBackupCollection</b> object.


## -parameters




### -param pIGPMSearchCriteria [in]

Pointer to the criteria to be applied to the search.



#### gpoDomain

Pointer to   the criteria for a search for a domain name.  The search property value is the domain name.  The <b>opEquals</b>
or <b>opNotEquals</b> operators are valid search criteria.



#### gpoID

Pointer to the criteria for a search for a Group Policy object (GPO) ID. The search property value is the GPO ID.  The <b>opEquals</b> or
<b>opNotEquals</b>  operators are valid search criteria.



#### gpoDisplayName

Pointer to the criteria for a search for   a GPO display name. The search property value is the GPO display name. The <b>opEquals</b>, 
<b>opContains</b>, or <b>opNotContains</b> operators are valid search criteria.



#### backupMostRecent

Pointer to the criteria for a search for the most recent backup. The search property value is <b>TRUE</b>. The   <b>opEquals</b>  operator is the valid criteria.


### -param pvarBackupCollection [out]

Pointer to the 
<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a> or <a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMStarterGPOBackupCollection</a> interface that represent the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> or <b>IGPMStarterGPOBackup</b> objects that are found by the search.


#### - objGPMSearchCriteria [in]


<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> object to apply to the search.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMBackupCollection</b> or <b>GPMStarterGPOBackupCollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMBackupCollection</b> or <b>GPMStarterGPOBackupCollection</b> object.




## -remarks



An empty  <a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a> interface or <b>GPMSearchCriteria</b> object has had no criteria added to it. Passing in an empty <b>IGPMSearchCriteria</b> interface or <b>GPMSearchCriteria</b> object will return all  
information in the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>
   or <b>IGPMStarterGPOBackup</b>
    interface.




## -see-also




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">IGPMBackupDirEx</a>



<b>IGPMStarterGPOBackup</b>



<b>IGPMStarterGPOBackupCollection</b>
 

 

