---
UID: NE:wcntypes.tagWCN_VALUE_TYPE_ASSOCIATION_STATE
title: tagWCN_VALUE_TYPE_ASSOCIATION_STATE
author: windows-driver-content
description: WCN_VALUE_TYPE_ASSOCIATION_STATE enumeration defines the possible association states of a wireless station during a Discovery request.
old-location: wcn\wcn_value_type_association_state.htm
old-project: wcn
ms.assetid: 0e225d34-d58e-49ae-8642-7070e3906fb3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WCN_VALUE_AS_ASSOCIATION_FAILURE, WCN_VALUE_AS_CONFIGURATION_FAILURE, WCN_VALUE_AS_CONNECTION_SUCCESS, WCN_VALUE_AS_IP_FAILURE, WCN_VALUE_AS_NOT_ASSOCIATED, WCN_VALUE_TYPE_ASSOCIATION_STATE, WCN_VALUE_TYPE_ASSOCIATION_STATE enumeration [Windows Connect Now], tagWCN_VALUE_TYPE_ASSOCIATION_STATE, wcn.wcn_value_type_association_state, wcntypes/WCN_VALUE_AS_ASSOCIATION_FAILURE, wcntypes/WCN_VALUE_AS_CONFIGURATION_FAILURE, wcntypes/WCN_VALUE_AS_CONNECTION_SUCCESS, wcntypes/WCN_VALUE_AS_IP_FAILURE, wcntypes/WCN_VALUE_AS_NOT_ASSOCIATED, wcntypes/WCN_VALUE_TYPE_ASSOCIATION_STATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wcntypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wcndevice.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WCN_VALUE_TYPE_ASSOCIATION_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wcntypes.h
api_name:
-	WCN_VALUE_TYPE_ASSOCIATION_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagWCN_VALUE_TYPE_ASSOCIATION_STATE enumeration


## -description


The <b>WCN_VALUE_TYPE_ASSOCIATION_STATE</b> enumeration defines the possible association states of a wireless station during a Discovery request.


## -enum-fields




### -field WCN_VALUE_AS_NOT_ASSOCIATED

The wireless station is not associated.


### -field WCN_VALUE_AS_CONNECTION_SUCCESS

The connection was successfully established.


### -field WCN_VALUE_AS_CONFIGURATION_FAILURE

The wireless station is not properly configured.


### -field WCN_VALUE_AS_ASSOCIATION_FAILURE

Association has failed.


### -field WCN_VALUE_AS_IP_FAILURE

 The specified IP address could not be connected to, and may be invalid.


## -see-also




<a href="https://msdn.microsoft.com/214b64c3-b1f0-46b1-b52a-b1df1bb40cf7">WCN_ATTRIBUTE_TYPE</a>
 

 

