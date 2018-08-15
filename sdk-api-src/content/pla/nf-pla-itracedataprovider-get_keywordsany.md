---
UID: NF:pla.ITraceDataProvider.get_KeywordsAny
title: ITraceDataProvider::get_KeywordsAny
author: windows-sdk-content
description: Retrieves the list of keywords that determine the category of events that you want the provider to write.
old-location: pla\itracedataprovider_keywordsany.htm
old-project: PLA
ms.assetid: 10159c09-609a-4263-a515-241ab942c3e8
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ITraceDataProvider interface [PLA],KeywordsAny property, ITraceDataProvider.KeywordsAny, ITraceDataProvider.get_KeywordsAny, ITraceDataProvider::KeywordsAny, ITraceDataProvider::get_KeywordsAny, KeywordsAny property [PLA], KeywordsAny property [PLA],ITraceDataProvider interface, get_KeywordsAny, pla.itracedataprovider_keywordsany, pla/ITraceDataProvider::KeywordsAny, pla/ITraceDataProvider::get_KeywordsAny
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: pla.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataProvider.KeywordsAny
 - ITraceDataProvider.get_KeywordsAny
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: ADAM
---

# ITraceDataProvider::get_KeywordsAny


## -description


Retrieves the list of keywords that determine the category of events that you want the provider to write.

This property is read-only.


## -parameters


## -remarks



Keywords determine the category of events that you want the provider to write. The provider writes an event if any of the event's keyword bits match any of the bits set in this <b>KeywordsAny</b> mask.

To include all events that a provider provides, set this property to zero. To include only specific events, set this keyword mask to those specific events. For example, if the provider defines an event for its initialization and clean-up routines (bit 0), an event for its file operations (bit 1), and an event for its calculation operations (bit 2), you can choose to include only two of these events by setting this mask to 5 (set bits 0 and 2) to receive initialization and clean-up events and calculation events.

To further restrict the category of events that you want the provider to write, also set the <a href="https://msdn.microsoft.com/9ff48234-927b-4b87-a9b8-2a1047b5e3de">ITraceDataProvider::KeywordsAll</a> property.

If the provider defines more complex event keywords (for example, the provider defines an event that sets bit 0 for read and bit 1 for local access and a second event that sets bit 0 for read and bit 2 for remote access), you could set this mask to 1 to receive all read events, or you could set this mask to 1 and the <a href="https://msdn.microsoft.com/9ff48234-927b-4b87-a9b8-2a1047b5e3de">KeywordsAll</a> mask to 3 to receive local reads only.

If an event's keyword is zero, the provider will write the event to the session, regardless of this mask or the <a href="https://msdn.microsoft.com/9ff48234-927b-4b87-a9b8-2a1047b5e3de">KeywordsAll</a> mask.



For providers that were written on an operating system prior to Windows Vista, the keyword value will be mapped to the enable flags.

You use the <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface to retrieve or set the keywords value. You can use the <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> property to retrieve the keywords value (the value of all of the items in the map when combined with the <b>OR</b> operator), or you can enumerate each item in the map to retrieve the individual keyword values.

Likewise, when you set the keywords value, you call the <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> property to set the keywords value, or you can call the <a href="https://msdn.microsoft.com/4a6f074d-8d18-44ea-bbbc-8d3a7f6c033a">IValueMap::Add</a> method to add each individual keyword value.

If you use <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> to set the keywords and the value map contains one or more items, PLA searches the collection for matching values and enables them and disables the others. If the value does not exist in the list, PLA adds the keyword (the item is not named).

The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property contains the string representation of the keyword. The <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the keyword value. The <a href="https://msdn.microsoft.com/f23e02bf-217a-44a2-9e1f-e92a39c1b065">IValueMapItem::Enabled</a> property indicates if the keyword is enabled.  You need to use the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface only when you want to name the keyword or you want to enable or disable keywords without having to add or remove them.




## -see-also




<a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a>



<a href="https://msdn.microsoft.com/9ff48234-927b-4b87-a9b8-2a1047b5e3de">ITraceDataProvider::KeywordsAll</a>
 

 

