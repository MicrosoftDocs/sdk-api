---
UID: NC:wsman.WSMAN_PLUGIN_AUTHORIZE_OPERATION
title: WSMAN_PLUGIN_AUTHORIZE_OPERATION (wsman.h)
description: Authorizes a specific operation.
helpviewer_keywords: ["Command","Create","Delete","Enumerate","Get","Invoke","Put","Shell","Subscribe","WSMAN_PLUGIN_AUTHORIZE_OPERATION","WSMAN_PLUGIN_AUTHORIZE_OPERATION callback","WSMAN_PLUGIN_AUTHORIZE_OPERATION callback function [Windows Management Instrumentation]","winrm.wsman_plugin_authorize_operation","wsman/WSMAN_PLUGIN_AUTHORIZE_OPERATION"]
old-location: winrm\wsman_plugin_authorize_operation.htm
tech.root: winrm
ms.assetid: 28fbd8db-557d-487b-8cf7-c550fe0826f7
ms.date: 12/05/2018
ms.keywords: Command, Create, Delete, Enumerate, Get, Invoke, Put, Shell, Subscribe, WSMAN_PLUGIN_AUTHORIZE_OPERATION, WSMAN_PLUGIN_AUTHORIZE_OPERATION callback, WSMAN_PLUGIN_AUTHORIZE_OPERATION callback function [Windows Management Instrumentation], winrm.wsman_plugin_authorize_operation, wsman/WSMAN_PLUGIN_AUTHORIZE_OPERATION
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSMAN_PLUGIN_AUTHORIZE_OPERATION
 - wsman/WSMAN_PLUGIN_AUTHORIZE_OPERATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wsman.h
api_name:
 - WSMAN_PLUGIN_AUTHORIZE_OPERATION
---

# WSMAN_PLUGIN_AUTHORIZE_OPERATION callback function


## -description

Authorizes a specific operation. 

The DLL entry point name for this method must be <b>WSManPluginAuthzOperation</b>.

## -parameters

### -param pluginContext [in]

Specifies the context that was returned by a call to <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_startup">WSManPluginStartup</a>. This parameter represents a specific application initialization of a WinRM plug-in.

### -param senderDetails [in]

A pointer  to the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_sender_details">WSMAN_SENDER_DETAILS</a> structure that specifies the identification information of the user.

### -param flags [in]

Reserved for future use. Must be set to zero.

### -param operation [in]

Represents the operation that is being performed. This parameter can be one of the following values:



#### Get

WSManOperationGet



#### Put

WSManOperationPut



#### Create

WSManOperationCreate



#### Delete

WSManOperationDelete



#### Enumerate

WSManOperationEnumerate



#### Subscribe

WSManOperationSubscribe



#### Shell

WSManOperationShell



#### Command

WSManOperationCommand



#### Invoke

WSManOperationInvoke

### -param action [in]

Specifies the action of the request received.  This parameter can be one of the following values:



#### Get

`http://schemas.xmlsoap.org/ws/2004/09/transfer/Get`



#### Put

`http://schemas.xmlsoap.org/ws/2004/09/transfer/Put`



#### Create

`http://schemas.xmlsoap.org/ws/2004/09/transfer/Create`

<div class="alert"><b>Note</b>  Shell creation will appear as Create.</div>
<div> </div>


#### Delete

`http://schemas.xmlsoap.org/ws/2004/09/transfer/Delete`



#### Enumerate

`http://schemas.xmlsoap.org/ws/2004/09/enumeration/Enumerate`



#### Subscribe

`http://schemas.xmlsoap.org/ws/2004/08/eventing/Subscribe`



#### Command

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell/Command`



#### Invoke

This operation will have a custom string.

### -param resourceUri [in]

Specifies the <a href="/windows/desktop/WinRM/windows-remote-management-glossary">resource URI</a> of the inbound operation.

## -remarks

The plug-in must call <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginauthzoperationcomplete">WSManPluginAuthzOperationComplete</a> to report either that the user was successfully authorized to perform the operation with <b>NO_ERROR</b> or that the user was not authorized with <b>ERROR_ACCESS_DENIED</b>. All other errors report a failure to the client, but no specific information is reported.
