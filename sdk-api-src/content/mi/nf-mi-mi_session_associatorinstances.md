---
UID: NF:mi.MI_Session_AssociatorInstances
title: MI_Session_AssociatorInstances function
author: windows-driver-content
description: Finds instances that are associated with the specific key instance.
old-location: wmi_v2\mi_session_associatorinstances.htm
old-project: wmi_v2
ms.assetid: 4e517289-a30e-4ba3-8cbf-dfc4f9744b1a
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: MI_Session_AssociatorInstances, MI_Session_AssociatorInstances function [Windows Management Infrastructure (MI)], mi/MI_Session_AssociatorInstances, wmi_v2.mi_session_associatorinstances
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Session_AssociatorInstances
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Session_AssociatorInstances function


## -description


Finds instances that are associated with the specific key instance.


## -parameters




### -param session [in]

Handle created from a call to <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


### -param flags

Runtime type information (RTTI) <a href="https://msdn.microsoft.com/24E82AC6-A2E3-4EC6-931F-26AC54D5CAA7">flags</a>.


### -param options [in, optional]

Optional <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> value that specifies options such as timeouts and how to control the CIM semantics. Specify NULL if no operation options are to be sent.


### -param namespaceName

A null-terminated string that contains the optional namespace name to carry out the operation.  If none is specified the server will pick a default.  The namespace cannot include a computer name.  It can only be in the form of namespace names separated by a slash character, for instance root/cimv2.


### -param instanceKey [in]

An <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> that represents the class name and the keys of the instance where the association will start.


### -param assocClass

A null-terminated string that represents the optional value that specifies to only map the association via this association class. If this value is NULL, then any association classes will be used.


### -param resultClass

A null-terminated string that represents the optional values that restricts the result set to only this class. Specify NULL if no filtering is wanted.


### -param role

A null-terminated string that represents the property name in the association object that points to our key object.


### -param resultRole

A null-terminated string that represents the property name in the association object that points to the resultant class.


### -param keysOnly

If set to MI_TRUE the operation will only retrieve the key properties of the instances. Otherwise, specify MI_FALSE.


### -param callbacks [in, optional]

Optional <a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. For asynchronous operation, the callback must be specified. For synchronous operation, specify NULL; the client must then call <a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a> to retrieve the results.


### -param operation [out]

Operation handle that must be closed with a call to <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a> once the operation is finished and all results have been received. The handle can be used to cancel the operation with a call to <a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>.


## -remarks



An association is a relationship between two objects. It is represented with a third object containing two properties, each being a reference to one of those two related objects. The <i>role</i> parameter is the association object's reference property, pointing to the object being associated. The <i>resultRole</i> parameter points to the other, resultant object.




## -see-also




<a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>



<a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>



<a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>



<a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a>
 

 

