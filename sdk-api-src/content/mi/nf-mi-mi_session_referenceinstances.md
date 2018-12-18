---
UID: NF:mi.MI_Session_ReferenceInstances
title: MI_Session_ReferenceInstances function
author: windows-sdk-content
description: Finds the association object that references the specified key instance.
old-location: wmi_v2\mi_session_referenceinstances.htm
tech.root: wmi_v2
ms.assetid: b42ed359-9580-4948-b29e-c5621a81206f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_Session_ReferenceInstances, MI_Session_ReferenceInstances function [Windows Management Infrastructure (MI)], mi/MI_Session_ReferenceInstances, wmi_v2.mi_session_referenceinstances
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Session_ReferenceInstances
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Session_ReferenceInstances function


## -description


Finds the association object that references the specified key instance.


## -parameters




### -param session [in]

Session handle returned from <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


### -param flags

Runtime type information (RTTI) <a href="https://msdn.microsoft.com/24E82AC6-A2E3-4EC6-931F-26AC54D5CAA7">flags</a>.


### -param options [in, optional]

Optional <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> value that specifies options such as timeouts and how to control the CIM semantics. Specify <b>Null</b> if no operation options are to be sent.


### -param namespaceName

An optional, null-terminated string that represents the namespace name to carry out the operation.  If none is specified, the server will pick a default.  The namespace cannot include a computer name.  It can only be in the form of a namespace name separated by a slash mark character (/). For example, the following would be a valid <b>namespaceName</b> value: <b>root/cimv2</b>.


### -param instanceKey [in]

An <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> that represents the class name and the keys of the instance where the reference operation is to start.


### -param resultClass

An optional, null-terminated string that represents the value that restricts the result set to only this association class. Specify <b>Null</b> if no filtering is wanted.


### -param role

An optional, null-terminated string that represents the value that specifies which property name in the association class to use to reference the key class.


### -param keysOnly

Boolean value where <b>MI_TRUE</b> means to retrieve only the instance keys. Otherwise, all properties will be retrieved.


### -param callbacks [in, optional]

Optional <a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. To carry out the operation asynchronously, the structure's <b>instanceResult</b> callback member must be specified. If that structure member is not specified, the client must call the <a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a> function to retrieve the results.


### -param operation [out]

Returned operation handle that must be closed via <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a> once complete.  Calling <a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a> before it is complete will cause the operation to shutdown.  <b>MI_Operation_Close</b> and <b>MI_Operation_Cancel</b> can be called from any operation.


## -remarks



An association is a relationship between two objects. It is represented with a third object containing two properties, each being a reference to one of those two related objects. The <i>role</i> parameter is the association object's reference property, pointing to the object being associated.

The difference between this function and the <a href="https://msdn.microsoft.com/4e517289-a30e-4ba3-8cbf-dfc4f9744b1a">MI_Session_AssociatorInstances</a> function is that this function looks for the association object itself, while the <b>MI_Session_AssociatorInstances</b> function looks for the instances associated with the key object.




## -see-also




<a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>



<a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a>



<a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>



<a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>



<a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a>



<a href="https://msdn.microsoft.com/4e517289-a30e-4ba3-8cbf-dfc4f9744b1a">MI_Session_AssociatorInstances</a>
 

 

