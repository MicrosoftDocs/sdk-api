---
UID: NS:ocidl.tagQACONTAINER
title: tagQACONTAINER
author: windows-sdk-content
description: Specifies container information for IQuickActivate::QuickActivate.
old-location: com\qacontainer.htm
tech.root: com
ms.assetid: 8f3975eb-7cd2-449f-92cc-2b8773d9f37e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: QACONTAINER, QACONTAINER structure [COM], _ctrl_QACONTAINER, com.qacontainer, ocidl/QACONTAINER, tagQACONTAINER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - OCIdl.h
api_name:
 - QACONTAINER
product: Windows
targetos: Windows
req.typenames: QACONTAINER
req.redist: 
---

# tagQACONTAINER structure


## -description


Specifies container information for <a href="https://msdn.microsoft.com/504cb272-da1c-4ffb-b4b1-fdf288901660">IQuickActivate::QuickActivate</a>.


## -struct-fields




### -field cbSize

The size of the structure, in bytes.


### -field pClientSite

A pointer to an <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a> interface in the container.


### -field pAdviseSink

A pointer to an <a href="https://msdn.microsoft.com/d1a52353-dd86-4083-9dbc-3a6f363a1a57">IAdviseSinkEx</a> interface in the container.


### -field pPropertyNotifySink

A pointer to an <a href="https://msdn.microsoft.com/bfdf315c-6375-4c77-abd8-03f07342820f">IPropertyNotifySink</a> interface in the container.


### -field pUnkEventSink

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the container's sink object.


### -field dwAmbientFlags

The number of ambient properties supplied by the container using values from the <a href="https://msdn.microsoft.com/bcca4762-7c4b-4062-8d41-6b2027045886">QACONTAINERFLAGS</a> enumeration.


### -field colorFore

Specifies ForeColor, an ambient property supplied by the container with a DISPID = -704.


### -field colorBack

Specifies BackColor, an ambient property supplied by the container with a DISPID = -701.


### -field pFont

Specifies Font, an ambient property supplied by the container with a DISPID = -703.


### -field pUndoMgr

A pointer to an <a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a> interface in the container.


### -field dwAppearance

Specifies Appearance, an ambient property supplied by the container with a DISPID = -716.


### -field lcid

Specifies LocaleIdentifier, an ambient property supplied by the container with a DISPID = -705.


### -field hpal

Specifies Palette, an ambient property supplied by the container with a DISPID = -726.


### -field pBindHost

A pointer to an <a href="_inet_IBindHost_Interface_cpp">IBindHost</a> interface in the container.


### -field pOleControlSite

A pointer to the <a href="https://msdn.microsoft.com/8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9">IOleControlSite</a> interface in the container's site object.


### -field pServiceProvider

A pointer to the <a href="_inet_IServiceProvider_Interface_cpp">IServiceProvider</a> interface in the container.


## -remarks



If an interface pointer in the <b>QACONTAINER</b> structure is <b>NULL</b> it does not indicate that the interface is not supported. In this situation, the control should use <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to obtain the interface pointer in the standard manner.




## -see-also




<a href="https://msdn.microsoft.com/504cb272-da1c-4ffb-b4b1-fdf288901660">IQuickActivate::QuickActivate</a>



<a href="https://msdn.microsoft.com/bcca4762-7c4b-4062-8d41-6b2027045886">QACONTAINERFLAGS</a>
 

 

