---
UID: NE:http._HTTP_VERB
title: HTTP_VERB (http.h)
description: The HTTP_VERB enumeration type defines values that are used to specify known, standard HTTP verbs in the HTTP_REQUEST structure. The majority of these known verbs are documented in RFC 2616 and RFC 2518, as indicated below.
helpviewer_keywords: ["*PHTTP_VERB","HTTP_VERB","HTTP_VERB enumeration [HTTP]","HttpVerbCONNECT","HttpVerbCOPY","HttpVerbDELETE","HttpVerbGET","HttpVerbHEAD","HttpVerbInvalid","HttpVerbLOCK","HttpVerbMKCOL","HttpVerbMOVE","HttpVerbMaximum","HttpVerbOPTIONS","HttpVerbPOST","HttpVerbPROPFIND","HttpVerbPROPPATCH","HttpVerbPUT","HttpVerbSEARCH","HttpVerbTRACE","HttpVerbTRACK","HttpVerbUNLOCK","HttpVerbUnknown","HttpVerbUnparsed","PHTTP_VERB","PHTTP_VERB enumeration pointer [HTTP]","_http_http_verb","http.http_verb","http/HTTP_VERB","http/HttpVerbCONNECT","http/HttpVerbCOPY","http/HttpVerbDELETE","http/HttpVerbGET","http/HttpVerbHEAD","http/HttpVerbInvalid","http/HttpVerbLOCK","http/HttpVerbMKCOL","http/HttpVerbMOVE","http/HttpVerbMaximum","http/HttpVerbOPTIONS","http/HttpVerbPOST","http/HttpVerbPROPFIND","http/HttpVerbPROPPATCH","http/HttpVerbPUT","http/HttpVerbSEARCH","http/HttpVerbTRACE","http/HttpVerbTRACK","http/HttpVerbUNLOCK","http/HttpVerbUnknown","http/HttpVerbUnparsed","http/PHTTP_VERB"]
old-location: http\http_verb.htm
tech.root: http
ms.assetid: 4aa36eab-eff2-4caa-9bad-15c534c5a5a0
ms.date: 12/05/2018
ms.keywords: '*PHTTP_VERB, HTTP_VERB, HTTP_VERB enumeration [HTTP], HttpVerbCONNECT, HttpVerbCOPY, HttpVerbDELETE, HttpVerbGET, HttpVerbHEAD, HttpVerbInvalid, HttpVerbLOCK, HttpVerbMKCOL, HttpVerbMOVE, HttpVerbMaximum, HttpVerbOPTIONS, HttpVerbPOST, HttpVerbPROPFIND, HttpVerbPROPPATCH, HttpVerbPUT, HttpVerbSEARCH, HttpVerbTRACE, HttpVerbTRACK, HttpVerbUNLOCK, HttpVerbUnknown, HttpVerbUnparsed, PHTTP_VERB, PHTTP_VERB enumeration pointer [HTTP], _http_http_verb, http.http_verb, http/HTTP_VERB, http/HttpVerbCONNECT, http/HttpVerbCOPY, http/HttpVerbDELETE, http/HttpVerbGET, http/HttpVerbHEAD, http/HttpVerbInvalid, http/HttpVerbLOCK, http/HttpVerbMKCOL, http/HttpVerbMOVE, http/HttpVerbMaximum, http/HttpVerbOPTIONS, http/HttpVerbPOST, http/HttpVerbPROPFIND, http/HttpVerbPROPPATCH, http/HttpVerbPUT, http/HttpVerbSEARCH, http/HttpVerbTRACE, http/HttpVerbTRACK, http/HttpVerbUNLOCK, http/HttpVerbUnknown, http/HttpVerbUnparsed, http/PHTTP_VERB'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
targetos: Windows
req.typenames: HTTP_VERB, *PHTTP_VERB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_VERB
 - http/_HTTP_VERB
 - PHTTP_VERB
 - http/PHTTP_VERB
 - HTTP_VERB
 - http/HTTP_VERB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_VERB
---

# HTTP_VERB enumeration


## -description

The 
<b>HTTP_VERB</b> enumeration type defines values that are used to specify known, standard HTTP verbs in the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure. The majority of these known verbs are  documented in <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a> and 
<a href="https://www.ietf.org/rfc/rfc2518.txt">RFC 2518</a>, as indicated below.

## -enum-fields

### -field HttpVerbUnparsed

Not relevant for applications; used only in kernel mode.

### -field HttpVerbUnknown

Indicates that the application can examine the <b>UnknownVerbLength</b> and <b>pUnknownVerb</b> members of the <a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure to retrieve the HTTP verb for the request.  This is the case in an HTTP/1.1 request when a browser client specifies a custom verb.

### -field HttpVerbInvalid

Not relevant for applications; used only in kernel mode.

### -field HttpVerbOPTIONS

The OPTIONS method requests information about the communication options  and requirements associated with a URI.


					See page 52 of <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

### -field HttpVerbGET

The GET method  retrieves the information or entity that is identified by the URI of the Request. If that URI refers to a script or other data-producing process, it is the data produced, not the text of the script, that is returned in the response.

A GET method can be made conditional or partial by including a conditional  or Range header field in the request. A conditional GET requests that the entity be sent only if all conditions specified in the header are met, and a partial GET requests only part of the entity, as specified in the Range header. Both of these forms of GET can help avoid unnecessary network traffic.


					See page 53 of <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

### -field HttpVerbHEAD

The HEAD method is identical to GET except that the server only returns message-headers in the response, without a message-body. The headers are the same as would be returned in response to a GET.


					See page 54 of <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

### -field HttpVerbPOST

The POST method is used to post a new entity as an addition to  a URI.
The URI identifies an entity that  consumes the posted data in some fashion.


					See page 54 of <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

### -field HttpVerbPUT

The PUT method is used to replace an entity identified by a URI.


					See page 55 of <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

### -field HttpVerbDELETE

The
					DELETE method requests that a specified URI be deleted.


					See page 56 of <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

### -field HttpVerbTRACE

The TRACE method invokes a remote, application-layer loop-back of the request message.
					It allows the client to see what is being received at the other
   end of the request chain for diagnostic
   purposes. See page 56 of <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

### -field HttpVerbCONNECT

The CONNECT
					method can be used with a proxy that can dynamically switch to tunneling, as in the case of SSL tunneling. See page 57 of <a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

### -field HttpVerbTRACK

The TRACK method is used by Microsoft Cluster Server to implement a non-logged trace.

### -field HttpVerbMOVE

The MOVE method requests a WebDAV operation
   equivalent to a copy (COPY), followed by consistency maintenance
   processing, followed by a delete of the source, where all three
   actions are performed atomically. When applied to a collection, "Depth" is assumed to be or must be specified as "infinity". See page 42 of <a href="https://www.ietf.org/rfc/rfc2518.txt">RFC 2518</a>.

### -field HttpVerbCOPY

The COPY method requests a WebDAV operation that creates a duplicate of the source resource,
   identified by the Request URI, in the destination resource,
   identified by a URI specified in the Destination header. See page 37 of <a href="https://www.ietf.org/rfc/rfc2518.txt">RFC 2518</a>.

### -field HttpVerbPROPFIND

The PROPFIND method requests a WebDAV operation that retrieves properties defined on the resource
   identified by the Request-URI. See page 24 of <a href="https://www.ietf.org/rfc/rfc2518.txt">RFC 2518</a>.

### -field HttpVerbPROPPATCH

The PROPPATCH method requests a WebDAV operation that sets and/or removes properties defined on the resource
   identified by the Request-URI. See page 31 of <a href="https://www.ietf.org/rfc/rfc2518.txt">RFC 2518</a>.

### -field HttpVerbMKCOL

The MKCOL method requests a WebDAV operation that creates a new collection
					 resource at the location specified by
   the Request-URI. See page 33 of <a href="https://www.ietf.org/rfc/rfc2518.txt">RFC 2518</a>.

### -field HttpVerbLOCK

The LOCK method requests a  WebDAV operation that creates a lock as specified by the lockinfo
   XML element on the Request-URI. See page 45 of <a href="https://www.ietf.org/rfc/rfc2518.txt">RFC 2518</a>.

### -field HttpVerbUNLOCK

The UNLOCK method requests a WebDAV operation that removes a lock, identified by a lock token in
   the Lock-Token request header, from the resource identified by the Request-URI, and from all other
   resources included in the lock. See page 51 of <a href="https://www.ietf.org/rfc/rfc2518.txt">RFC 2518</a>.

### -field HttpVerbSEARCH

The SEARCH method requests a WebDAV operation used by
					Microsoft Exchange to search folders. See the Internet Engineering Task Force (IETF) Internet Draft WebDAV SEARCH for more information, and the <a href="http://www.webdav.org/">WebDAV Web site</a> for possible updates.

### -field HttpVerbMaximum

Terminates the enumeration; is not used to define a verb.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>