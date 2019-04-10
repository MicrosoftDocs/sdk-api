---
UID: NE:oleidl.tagOLEUPDATE
title: OLEUPDATE (oleidl.h)
author: windows-sdk-content
description: Indicates whether the linked object updates the cached data for the linked object automatically or only when the container calls either the IOleObject::Update or IOleLink::Update methods. The constants are used in the IOleLink interface.
old-location: com\oleupdate.htm
tech.root: com
ms.assetid: 1945d4a2-dd1f-453e-ab7e-093f26171c84
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPOLEUPDATE, *POLEUPDATE, LPOLEUPDATE, LPOLEUPDATE enumeration pointer [COM], OLEUPDATE, OLEUPDATE enumeration [COM], OLEUPDATE_ALWAYS, OLEUPDATE_ONCALL, POLEUPDATE, POLEUPDATE enumeration pointer [COM], _ole_OLEUPDATE, com.oleupdate, oleidl/LPOLEUPDATE, oleidl/OLEUPDATE, oleidl/OLEUPDATE_ALWAYS, oleidl/OLEUPDATE_ONCALL, oleidl/POLEUPDATE"
ms.topic: enum
req.header: oleidl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLEUPDATE
product: Windows
targetos: Windows
req.typenames: OLEUPDATE
req.redist: 
---

# OLEUPDATE enumeration


## -description


Indicates whether the linked object updates the cached data for the linked object automatically or only when the container calls either the <a href="https://msdn.microsoft.com/1743f99b-4c3b-47be-b77b-1d3378a44903">IOleObject::Update</a> or <a href="https://msdn.microsoft.com/c1da8b95-88e7-42b0-884c-5aa394cc49f4">IOleLink::Update</a> methods. The constants are used in the <a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a> interface. 




## -enum-fields




### -field OLEUPDATE_ALWAYS

Update the link object whenever possible, this option corresponds to the <b>Automatic update</b> option in the <b>Links</b> dialog box.


### -field OLEUPDATE_ONCALL

Update the link object only when <a href="https://msdn.microsoft.com/1743f99b-4c3b-47be-b77b-1d3378a44903">IOleObject::Update</a> or <a href="https://msdn.microsoft.com/c1da8b95-88e7-42b0-884c-5aa394cc49f4">IOleLink::Update</a> is called, this option corresponds to the <b>Manual update</b> option in the <b>Links</b> dialog box.



## -see-also




<a href="https://msdn.microsoft.com/2cb91b48-0026-4afa-80ab-16ac6fbce04d">IOleLink::GetUpdateOptions</a>



<a href="https://msdn.microsoft.com/310c25b5-a2f6-4ed7-8673-c53809fad32f">IOleLink::SetUpdateOptions</a>
 

 

