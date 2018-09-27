---
UID: NS:oledlg.tagOLEUIGNRLPROPSA
title: tagOLEUIGNRLPROPSA
author: windows-sdk-content
description: Initializes the General tab of the Object Properties dialog box.
old-location: com\oleuignrlprops_struct.htm
tech.root: com
ms.assetid: 851d66c8-94a7-47ab-95f4-12a34897de20
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPOLEUIGNRLPROPSA, *POLEUIGNRLPROPSA, LPOLEUIGNRLPROPS, LPOLEUIGNRLPROPS structure pointer [COM], OLEUIGNRLPROPS, OLEUIGNRLPROPS structure [COM], OLEUIGNRLPROPSA, OLEUIGNRLPROPSW, POLEUIGNRLPROPS, POLEUIGNRLPROPS structure pointer [COM], _ole_OLEUIGNRLPROPS, com.oleuignrlprops_struct, oledlg/LPOLEUIGNRLPROPS, oledlg/OLEUIGNRLPROPS, oledlg/OLEUIGNRLPROPSA, oledlg/OLEUIGNRLPROPSW, oledlg/POLEUIGNRLPROPS, tagOLEUIGNRLPROPSA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIGNRLPROPSW (Unicode) and OLEUIGNRLPROPSA (ANSI)
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
 - OLEUIGNRLPROPS
 - OLEUIGNRLPROPSA
 - OLEUIGNRLPROPSW
product: Windows
targetos: Windows
req.typenames: OLEUIGNRLPROPSA, *POLEUIGNRLPROPSA, *LPOLEUIGNRLPROPSA
req.redist: 
---

# tagOLEUIGNRLPROPSA structure


## -description


Initializes the <b>General</b> tab of the <b>Object Properties</b> dialog box. A reference to it is passed in as part of the <a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a> structure to the <a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a> function. This tab shows the type and size of an OLE embedding and allows it the user to tunnel to the <b>Convert</b> dialog box. This tab also shows the link destination if the object is a link.


## -struct-fields




### -field cbStruct

The size of the structure, in bytes. This field must be filled on input.


### -field dwFlags

Currently no flags associated with this member. It should be set to 0 (zero).


### -field dwReserved1

This member is reserved.


### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed.


### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the <b>lpfnHook</b> member during WM_INITDIALOG.


### -field dwReserved2

This member is reserved.


### -field lpOP

Used internally.


## -see-also




<a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a>



<a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a>
 

 

