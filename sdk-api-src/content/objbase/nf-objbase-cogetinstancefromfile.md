---
UID: NF:objbase.CoGetInstanceFromFile
title: CoGetInstanceFromFile function
author: windows-sdk-content
description: Creates a new object and initializes it from a file using IPersistFile::Load.
old-location: com\cogetinstancefromfile.htm
tech.root: com
ms.assetid: f8a22f5f-a21f-49e7-bd6c-ca987206ee46
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CoGetInstanceFromFile, CoGetInstanceFromFile function [COM], _com_CoGetInstanceFromFile, com.cogetinstancefromfile, objbase/CoGetInstanceFromFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Ole32.lib
req.dll: ComBase.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoGetInstanceFromFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoGetInstanceFromFile function


## -description


Creates a new object and initializes it from a file using <a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">IPersistFile::Load</a>.


## -parameters




### -param pServerInfo [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/88c94a7f-5cf0-4d61-833f-91cba45d8624">COSERVERINFO</a> structure that specifies the computer on which to instantiate the object and the authentication setting to be used. This parameter can be <b>NULL</b>, in which case the object is instantiated on the current computer, at the computer specified under the <a href="https://msdn.microsoft.com/0413564e-e8ba-4e6e-ad29-62997c63aab3">RemoteServerName</a> registry value for the class, or at the computer where the <i>pwszName</i> file resides if the <a href="https://msdn.microsoft.com/bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb">ActivateAtStorage</a> value is specified for the class or there is no local registry information.


### -param pClsid [in, optional]

A pointer to the class identifier of the object to be created. This parameter can be <b>NULL</b>, in which case there is a call to <a href="https://msdn.microsoft.com/dc3cb263-7b9a-45f9-8eab-3a88aa9392db">GetClassFile</a>, using <i>pwszName</i> as its parameter to get the class of the object to be instantiated.


### -param punkOuter [in, optional]

When non-<b>NULL</b>, indicates the instance is being created as part of an aggregate, and <i>punkOuter</i> is to be used as the pointer to the new instance's controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. Aggregation is not supported cross-process or cross-computer. When instantiating an object out of process, CLASS_E_NOAGGREGATION will be returned if <i>punkOuter</i> is non-<b>NULL</b>.


### -param dwClsCtx [in]

Values from the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration.


### -param grfMode [in]

Specifies how the file is to be opened. See <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>.


### -param pwszName [in]

The file used to initialize the object with <a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">IPersistFile::Load</a>. This parameter cannot be <b>NULL</b>.


### -param dwCount [in]

The number of structures in <i>pResults</i>. This parameter must be greater than 0.


### -param pResults [in, out]

An array of <a href="https://msdn.microsoft.com/845040c9-fad4-4ac8-856d-d35edbf48ec9">MULTI_QI</a> structures. Each structure has three members: the identifier for a requested interface (<b>pIID</b>), the location to return the interface pointer (<b>pItf</b>) and the return value of the call to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> (<b>hr</b>).


## -returns



This function can return the standard return value E_INVALIDARG, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function retrieved all of the interfaces successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_S_NOTALLINTERFACES</b></dt>
</dl>
</td>
<td width="60%">
At least one, but not all of the interfaces requested in the <i>pResults</i> array were successfully retrieved. The <b>hr</b> member of each of the <a href="https://msdn.microsoft.com/845040c9-fad4-4ac8-856d-d35edbf48ec9">MULTI_QI</a> structures indicates with S_OK or E_NOINTERFACE whether the specific interface was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
None of the interfaces requested in the <i>pResults</i> array were successfully retrieved.

</td>
</tr>
</table>
 




## -remarks



<b>CoGetInstanceFromFile</b> creates a new object and initializes it from a file using <a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">IPersistFile::Load</a>. The result of this function is similar to creating an instance with a call to <a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>, followed by an initializing call to <b>IPersistFile::Load</b>, with the following important distinctions:

<ul>
<li>Fewer network round trips are required by this function when instantiating an object on a remote computer.</li>
<li>In the case where <i>dwClsCtx</i> is set to CLSCTX_REMOTE_SERVER and <i>pServerInfo</i> is <b>NULL</b>, if the class is registered with the <a href="https://msdn.microsoft.com/bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb">ActivateAtStorage</a> sub-key or has no associated registry information, this function will instantiate an object on the computer where <i>pwszName</i> resides, providing the least possible network traffic.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a>



<a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>



<a href="https://msdn.microsoft.com/6a77770c-b7e1-4d29-9c4b-331b5950a635">CoGetInstanceFromIStorage</a>
 

 

