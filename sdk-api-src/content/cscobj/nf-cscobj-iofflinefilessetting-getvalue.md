---
UID: NF:cscobj.IOfflineFilesSetting.GetValue
title: IOfflineFilesSetting::GetValue
author: windows-sdk-content
description: Retrieves the value of a particular Offline Files setting.
old-location: of\iofflinefilessetting_getvalue.htm
tech.root: OfflineFiles
ms.assetid: 39560ca6-62d7-467b-bc52-1dd769e7e860
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetValue, GetValue method [Offline Files], GetValue method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetValue method, IOfflineFilesSetting.GetValue, IOfflineFilesSetting::GetValue, cscobj/IOfflineFilesSetting::GetValue, of.iofflinefilessetting_getvalue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSetting.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSetting::GetValue


## -description


Retrieves the value of a particular Offline Files setting.


## -parameters




### -param pvarValue [out]

Receives the value associated with the setting.  This value is determined based on system policy, preferences and system defaults.

The method initializes the <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> prior to storing the setting value in it.


### -param pbSetByPolicy [out]

Receives <b>TRUE</b> if the value was set by policy, <b>FALSE</b> if the value was determined by preference or default.


## -returns



<b>S_OK</b> if the value query is successful or an error value otherwise.




## -remarks



The value returned in the <i>pvarValue</i> parameter is determined as follows:

<ol>
<li>If machine policy exists, use it.</li>
<li>Otherwise, if user policy exists, use it.</li>
<li>Otherwise, if machine preference exists, use it.</li>
<li>Otherwise, if user preference exists, use it.</li>
<li>Otherwise, use the system default value.</li>
</ol>
The primary intent of the <i>pbSetByPolicy</i> parameter is to allow the caller to disable UI associated with a setting when the setting has been configured through Group Policy.

It is important to note that policy cannot be set through the Offline Files API.  Policy can be set only through the Group Policy mechanism.  The Offline Files API only supports querying policy values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530601(v=VS.85).aspx">IOfflineFilesSetting</a>
 

 

