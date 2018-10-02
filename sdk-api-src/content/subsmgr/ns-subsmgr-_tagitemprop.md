---
UID: NS:subsmgr._tagITEMPROP
title: "_tagITEMPROP"
author: windows-sdk-content
description: Stores information about properties in the Windows Property System, and is used by the IItemPropertyBag interface.
old-location: search\itemprop.htm
tech.root: search
ms.assetid: 480C84CB-60CE-42F4-ADE6-4FCF1EAF15AF
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: "*LPITEMPROP, ITEMPROP, ITEMPROP structure [search], PITEMPROP, PITEMPROP structure pointer [search], _tagITEMPROP, search.itemprop, subsmgr/ITEMPROP, subsmgr/PITEMPROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: subsmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - subsmgr.h
api_name:
 - ITEMPROP
product: Windows
targetos: Windows
req.typenames: ITEMPROP, *LPITEMPROP
req.redist: Windows Desktop Search (WDS) 3.0
---

# _tagITEMPROP structure


## -description


<p class="CCE_Message">[<b>ITEMPROP</b> and <a href="https://msdn.microsoft.com/0fef34c5-f20f-475a-9223-5cb73079c842">IItemPropertyBag</a> are supported only on Windows XP and Windows Server 2003, and should no longer be used.]

Stores information about properties in the <a href="https://msdn.microsoft.com/c2094bbe-a4ca-4f30-b16e-14dced2912bc">Windows Property System</a>, and is used by the <a href="https://msdn.microsoft.com/0fef34c5-f20f-475a-9223-5cb73079c842">IItemPropertyBag</a> interface.


## -struct-fields




### -field variantValue

 


### -field pwszName

 




#### - bstrIndexProp

The name of a property in the <a href="https://msdn.microsoft.com/c2094bbe-a4ca-4f30-b16e-14dced2912bc">Windows Property System</a>. For example, the <a href="https://msdn.microsoft.com/d592f12b-f8c2-406f-a031-eeb8212e64f7">System.ItemUrl</a> property.


#### - bstrName

For internal use only.


#### - ds

For internal use only.


#### - dwHint

For internal use only.


#### - dwUID

For internal use only.


#### - vt

The type of the property value. For example, the type of the string property <a href="https://msdn.microsoft.com/d592f12b-f8c2-406f-a031-eeb8212e64f7">System.ItemUrl</a> is <b>VT_BSTR</b>. 


## -remarks



To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the <a href="https://msdn.microsoft.com/0fef34c5-f20f-475a-9223-5cb73079c842">IItemPropertyBag</a> interface and the following APIs: the <a href="https://msdn.microsoft.com/en-us/library/Dd756719(v=VS.85).aspx">ISearchProtocolUI</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd561904(v=VS.85).aspx">IItemPreviewerExt</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd756722(v=VS.85).aspx">ISearchItem</a> interfaces, the <a href="https://msdn.microsoft.com/en-us/library/Dd561894(v=VS.85).aspx">LINKINFO</a> and <b>ITEMPROP</b> structures, and the <a href="https://msdn.microsoft.com/en-us/library/Dd561982(v=VS.85).aspx">LINKTYPE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/0fef34c5-f20f-475a-9223-5cb73079c842">IItemPropertyBag</a>
 

 

