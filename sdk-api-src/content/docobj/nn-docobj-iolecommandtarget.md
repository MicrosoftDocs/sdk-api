---
UID: NN:docobj.IOleCommandTarget
title: IOleCommandTarget (docobj.h)
description: Enables objects and their containers to dispatch commands to each other. For example, an object's toolbars may contain buttons for commands such as Print, Print Preview, Save, New, and Zoom.
helpviewer_keywords: ["IOleCommandTarget","IOleCommandTarget interface [COM]","IOleCommandTarget interface [COM]","described","_ole_iolecommandtarget","com.iolecommandtarget","docobj/IOleCommandTarget"]
old-location: com\iolecommandtarget.htm
tech.root: com
ms.assetid: 5c8b455e-7740-4f71-aef6-27390a11a1a3
ms.date: 12/05/2018
ms.keywords: IOleCommandTarget, IOleCommandTarget interface [COM], IOleCommandTarget interface [COM],described, _ole_iolecommandtarget, com.iolecommandtarget, docobj/IOleCommandTarget
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
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
 - IOleCommandTarget
 - docobj/IOleCommandTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleCommandTarget
---

# IOleCommandTarget interface


## -description

Enables objects and their containers to dispatch commands to each other. For example, an object's toolbars may contain buttons for commands such as <b>Print</b>, <b>Print Preview</b>, <b>Save</b>, <b>New</b>, and <b>Zoom</b>.

Normal in-place activation guidelines recommend that you remove or disable such buttons because no efficient, standard mechanism has been available to dispatch them to the container. Similarly, a container has heretofore had no efficient means to send commands such as <b>Print</b>, <b>Page Setup</b>, and <b>Properties</b> to an in-place active object. Such simple command routing could have been handled through existing OLE Automation standards and the <b>IDispatch</b> interface, but the overhead with IDispatch is more than is required in the case of document objects. The <b>IOleCommandTarget</b> interface provides a simpler means to achieve the same ends.

Available commands are defined by integer identifiers in a group. The group itself is identified with a GUID. The interface allows a caller both to query for support of one or more commands within a group and to issue a supported command to the object.

## -inheritance

The <b>IOleCommandTarget</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleCommandTarget</b> also has these types of members:

