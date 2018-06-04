---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WS_TYPE_MAPPING enumeration


## -description


How a <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a> maps to or from XML when serialized
                or deserialized.
            


## -enum-fields




### -field WS_ELEMENT_TYPE_MAPPING


                    This is used when reading or writing an element where the type
                    corresponds to the type of the element.
                    The definition of the type may include mappings to attributes,
                    text, or child elements of the element.
                


                    The following calling sequence is used when writing an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsWriteStartElement(...)
WsWriteType(..., WS_ELEMENT_TYPE_MAPPING, ...)
WsWriteEndElement(...)</code></pre>

                    The following calling sequence is used when reading an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsReadToStartElement(...)?
WsReadType(..., WS_ELEMENT_TYPE_MAPPING, ...)</code></pre>

### -field WS_ATTRIBUTE_TYPE_MAPPING


                    This is used when reading or writing the value of a single attribute.  The definition
                    of the type must not require any mappings to attributes or child elements.
                


                    The following calling sequence is used when writing an attribute value.
                

<pre class="syntax" xml:space="preserve"><code>
WsWriteStartAttribute(...)
WsWriteType(..., WS_ATTRIBUTE_TYPE_MAPPING, ...)
WsWriteEndAttribute(...)</code></pre>

                    The following calling sequence is used when reading an attribute value.
                

<pre class="syntax" xml:space="preserve"><code>
WsFindAttribute(...)
WsReadStartAttribute(...)
WsReadType(..., WS_ATTRIBUTE_TYPE_MAPPING, ...)
WsReadEndAttribute(...)</code></pre>

### -field WS_ELEMENT_CONTENT_TYPE_MAPPING


                    This is used when when the type corresponds to all or part of the 
                    content (text and child elements) of an element.
                    The definition of the type may include mappings to text or child
                    elements, but must not include any attributes.
                


                    The following calling sequence is used when writing the contents
                    of an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsWriteStartElement(...)
// Write attributes, if any
// Write other element content, if any
WsWriteType(..., WS_ELEMENT_CONTENT_TYPE_MAPPING, ...)
// Write other element content, if any
WsWriteEndElement(...)</code></pre>

                    The following calling sequence is used when reading the contents of
                    an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsReadToStartElement(...)
// Read attributes, if any
WsReadStartElement(...)
// Read other element content, if any
WsReadType(..., WS_ELEMENT_CONTENT_TYPE_MAPPING, ...)
// Read other element content, if any
WsReadEndElement(...)</code></pre>

### -field WS_ANY_ELEMENT_TYPE_MAPPING


                    This is used when when the type corresponds to the complete
                    element, including the name and namespace of the element.
                    The definition may include attributes and child elements
                    and text.
                


                    The following calling sequence is used when writing 
                    an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsWriteType(..., WS_ANY_ELEMENT_TYPE_MAPPING, ...)</code></pre>

                    The following calling sequence is used when reading the contents of
                    an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsReadToStartElement(...)?
WsReadType(..., WS_ANY_ELEMENT_TYPE_MAPPING, ...)</code></pre>

## -remarks




                See the documentation for each <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a> 
                for which <b>WS_TYPE_MAPPING</b> values are supported.
            



