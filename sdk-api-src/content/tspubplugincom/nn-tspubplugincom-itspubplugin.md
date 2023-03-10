---
UID: NN:tspubplugincom.ItsPubPlugin
title: ItsPubPlugin (tspubplugincom.h)
description: Exposes properties and methods that provide information about resources available to users of RemoteApp and Desktop Connections.
helpviewer_keywords: ["ItsPubPlugin","ItsPubPlugin interface [Remote Desktop Services]","ItsPubPlugin interface [Remote Desktop Services]","described","termserv.itspubplugin","tspubplugincom/ItsPubPlugin"]
old-location: termserv\itspubplugin.htm
tech.root: TermServ
ms.assetid: 37d33f27-a811-4c97-bc80-ff8a5b8fcb7c
ms.date: 12/05/2018
ms.keywords: ItsPubPlugin, ItsPubPlugin interface [Remote Desktop Services], ItsPubPlugin interface [Remote Desktop Services],described, termserv.itspubplugin, tspubplugincom/ItsPubPlugin
req.header: tspubplugincom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Cpubplugin.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ItsPubPlugin
 - tspubplugincom/ItsPubPlugin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tspubplugincom.h
api_name:
 - ItsPubPlugin
---

# ItsPubPlugin interface


## -description

Exposes properties and methods that provide information about resources available to users of RemoteApp and Desktop Connections. The methods in this interface are called by the RemoteApp and Desktop Connection Management service in Remote Desktop Web Access (RD Web Access) and Remote Desktop Connection Broker (RD Connection Broker).

Resources that can be exposed through <b>ItsPubPlugin</b> typically include RemoteApp programs, virtual machine pools, and personal virtual desktops. By implementing this interface and registering it in the Registry, these resources can be displayed to users in RD Web Access and RemoteApp and Desktop Connections.  Your interface can perform custom filtering of resources and provide support for file types that are not currently supported. (Only .rdp files are supported by default.)

## -inheritance

The <b>ItsPubPlugin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ItsPubPlugin</b> also has these types of members:

## -remarks

<p class="proch"><b>To register your plug-in so that it will be called by the RemoteApp and Desktop Connection Management service</b>

<ol>
<li>Implement the plug-in in a DLL and register the DLL by using the Regsvr32.exe tool.</li>
<li>Create a subkey named for the CLSID of the DLL under the following key:<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>Terminal Server</b>
                  <b>CentralizedPublishing</b>
                     <b>Plugins</b></pre>
</li>
<li>Create a value for the subkey of type <b>DWORD</b> with the name "IsEnabled". To allow the service to call the plug-in, set the value to one. To disallow calls to the plug-in, set the value to zero. You do not need to restart the service because the service loads the plug-in automatically.</li>
</ol>

## -see-also

<a href="/windows/desktop/TermServ/remoteapp-and-desktop-connection-management-service-interfaces">RemoteApp and Desktop Connection Management Service Interfaces</a>



<a href="/windows/desktop/TermServ/remoteapp-and-desktop-connection-management-service-structures">RemoteApp and Desktop Connection Management Service Structures</a>
