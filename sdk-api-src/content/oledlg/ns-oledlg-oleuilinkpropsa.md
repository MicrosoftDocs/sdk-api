---
UID: NS:oledlg.tagOLEUILINKPROPSA
title: OLEUILINKPROPSA (oledlg.h)
author: windows-sdk-content
description: Contains information that is used to initialize the Link tab of the Object Properties dialog box.
old-location: com\oleuilinkprops_struct.htm
tech.root: com
ms.assetid: 3f355ce8-adc3-4878-a8b4-3f7d94547ef1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPOLEUILINKPROPSA, *POLEUILINKPROPSA, LPOLEUILINKPROPS, LPOLEUILINKPROPS structure pointer [COM], OLEUILINKPROPS, OLEUILINKPROPS structure [COM], OLEUILINKPROPSA, OLEUILINKPROPSW, POLEUILINKPROPS, POLEUILINKPROPS structure pointer [COM], _ole_OLEUILINKPROPS, com.oleuilinkprops_struct, oledlg/LPOLEUILINKPROPS, oledlg/OLEUILINKPROPS, oledlg/OLEUILINKPROPSA, oledlg/OLEUILINKPROPSW, oledlg/POLEUILINKPROPS"
ms.topic: struct
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUILINKPROPSW (Unicode) and OLEUILINKPROPSA (ANSI)
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
 - OleDlg.h
api_name:
 - OLEUILINKPROPS
 - OLEUILINKPROPSA
 - OLEUILINKPROPSW
product: Windows
targetos: Windows
req.typenames: OLEUILINKPROPSA, *POLEUILINKPROPSA, *LPOLEUILINKPROPSA
req.redist: 
---

# OLEUILINKPROPSA structure


## -description


Contains information that is used to initialize the <b>Link</b> tab of the <b>Object Properties</b> dialog box. A reference to it is passed in as part of the <a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a> structure to the <a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a> function. This tab shows the location, update status, and update time for a link. It allows the user to change the source of the link, toggle its update status between automatic and manual update, open the source, force an update of the link, or break the link (convert it to a static picture).


## -struct-fields




### -field cbStruct

The size of the structure, in bytes.


### -field dwFlags

Contains in/out flags specific to the <b>Links</b> page.


### -field dwReserved1

This member is reserved.


### -field lpfnHook

Pointer to the hook callback (not used in this dialog box).


### -field lCustData

Custom data to pass to hook (not used in this dialog box).


### -field dwReserved2

This member is reserved.


### -field lpOP

Used internally.


## -see-also




<a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a>



<a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a>
 

 

