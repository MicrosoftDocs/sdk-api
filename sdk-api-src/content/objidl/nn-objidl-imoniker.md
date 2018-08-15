---
UID: NN:objidl.IMoniker
title: IMoniker
author: windows-sdk-content
description: Enables you to use a moniker object, which contains information that uniquely identifies a COM object.
old-location: com\imoniker.htm
old-project: com
ms.assetid: 17f4c1df-7a9c-42ef-a888-70cd8d85f070
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IMoniker, IMoniker interface [COM], IMoniker interface [COM],described, _com_imoniker, com.imoniker, objidl/IMoniker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMoniker
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IMoniker interface


## -description


Enables you to use a moniker object, which contains information that uniquely identifies a COM object. An object that has a pointer to the moniker object's <b>IMoniker</b> interface can locate, activate, and get access to the identified object without having any other specific information on where the object is actually located in a distributed system.

Monikers are used as the basis for linking in COM. A linked object contains a moniker that identifies its source. When the user activates the linked object to edit it, the moniker is bound; this loads the link source into memory. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMoniker</b> interface inherits from <b>IPersistStream</b>. <b>IMoniker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMoniker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">BindToObject</a>
</td>
<td align="left" width="63%">
Binds to the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94c8219f-8131-45dd-b350-878ffd6161ea">BindToStorage</a>
</td>
<td align="left" width="63%">
Binds to the storage for the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef2a3191-7b7c-4e51-ab55-cf601f444561">CommonPrefixWith</a>
</td>
<td align="left" width="63%">
Creates a new moniker based on the prefix that this moniker has in common with the specified moniker.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">ComposeWith</a>
</td>
<td align="left" width="63%">
Creates a new composite moniker by combining the current moniker with the specified moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e2e4d92-d5dd-4294-944e-8b1e88901ee1">Enum</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an enumerator for the components of a composite moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/424036c9-c097-4507-b562-4a01f9199b1f">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for the moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/120cc951-6797-4ef6-890b-57ff8d3d23ba">GetTimeOfLastChange</a>
</td>
<td align="left" width="63%">
Retrieves the time at which the object identified by this moniker was last changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5073c909-d3bc-480e-97fb-d096e60787e5">Hash</a>
</td>
<td align="left" width="63%">
Creates a hash value using the internal state of the moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/351d5da3-043b-426a-99e9-9f882f552239">Inverse</a>
</td>
<td align="left" width="63%">
Creates a moniker that is the inverse of this moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0092e93e-d87d-4b3e-b8e1-40eeaf04c43b">IsEqual</a>
</td>
<td align="left" width="63%">
Determines whether this moniker is identical to the specified moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/081b394c-1fe8-4519-999e-b3985a77bd9c">IsRunning</a>
</td>
<td align="left" width="63%">
Determines whether the object identified by this moniker is currently loaded and running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a61c0df9-786e-45e7-8b3d-f950decc596d">IsSystemMoniker</a>
</td>
<td align="left" width="63%">
Determines whether this moniker is one of the system-provided moniker classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a5a1f14-f14f-404b-90d8-0afceafc087c">ParseDisplayName</a>
</td>
<td align="left" width="63%">
Converts a display name into a moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d34da7b-e6cb-4daa-a155-45beb36e035b">Reduce</a>
</td>
<td align="left" width="63%">
Reduces a moniker to its simplest form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92e2e7d7-043e-4e95-8540-5a895b5a54f9">RelativePathTo</a>
</td>
<td align="left" width="63%">
Creates a relative moniker between this moniker and the specified moniker.

</td>
</tr>
</table> 


## -remarks



Like a path to a file in a file system, a moniker contains information that allows a COM object to be located and activated. Monikers can identify any type of COM object, from a document object stored in a file to a selection within an embedded object. COM provides a set of moniker classes that allow you to create moniker objects identifying the objects most commonly found in the system. For example, there might be an object representing a range of cells in a spreadsheet that is itself embedded in a text document stored in a file. In a distributed system, this object's moniker would identify the location of the object's system, the file's physical location on that system, the storage of the embedded object within that file, and, finally, the location of the range of cells within the embedded object.



A moniker object supports the <b>IMoniker</b> interface, which is derived from the <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> interface and uniquely identifies a single object in the system. After an object providing a moniker has created the moniker object, this information cannot be changed within that object. If the moniker provider changes the information, it can do so only by creating a new moniker object, which would then uniquely identify the object in question.

Monikers have the following two important capabilities: 



<ul>
<li>Monikers can be saved to a persistent storage. When a moniker is loaded back into memory, it still identifies the same object.</li>
<li>Monikers support an operation called binding, which is the process of locating the object named by the moniker, activating it (loading it into memory) if it is not already active, and returning a pointer to a requested interface on that object.</li>
</ul>
<h3><a id="Anti-Moniker_Implementation"></a><a id="anti-moniker_implementation"></a><a id="ANTI-MONIKER_IMPLEMENTATION"></a>Anti-Moniker Implementation</h3>
Anti-monikers are the inverse of the COM implementations of file, item, and pointer monikers. That is, an anti-moniker composed to the right of a file moniker, item moniker, or pointer moniker composes to nothing.

If you're a moniker client, you typically do not need to use anti-monikers. When you need the inverse of a moniker, you should call <a href="https://msdn.microsoft.com/351d5da3-043b-426a-99e9-9f882f552239">IMoniker::Inverse</a>. For example, if you need an inverse to remove the last piece of a composite moniker, use <a href="https://msdn.microsoft.com/7e2e4d92-d5dd-4294-944e-8b1e88901ee1">IMoniker::Enum</a> to enumerate the pieces of the moniker and call <b>Inverse</b> on the rightmost piece. You should not use an anti-moniker for this purpose because you cannot be sure that the right-most piece of a composite considers an anti-moniker to be its inverse.

The only situation in which you should explicitly use an anti-moniker is when you are writing a new moniker class and you have no special requirements for constructing inverses to your monikers. In that situation, you can return anti-monikers from your implementation of <a href="https://msdn.microsoft.com/351d5da3-043b-426a-99e9-9f882f552239">Inverse</a>. In your implementation of <a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">IMoniker::ComposeWith</a>, you should then annihilate one of your monikers for every anti-moniker you encounter.

Use the <a href="https://msdn.microsoft.com/1f8fcbd6-8f05-4d32-af8a-d8de1b56dacf">CreateAntiMoniker</a> function to create these monikers.

<h3><a id="Class_Moniker_Implementation"></a><a id="class_moniker_implementation"></a><a id="CLASS_MONIKER_IMPLEMENTATION"></a>Class Moniker Implementation</h3>
Class monikers are monikers that represent an object class. Class monikers bind to the class object of the class for which they are created.

Class monikers are most useful in composition with other types of monikers, such as file monikers or item monikers. Class monikers may also be composed to the right of monikers supporting binding to the <a href="https://msdn.microsoft.com/4f34c5a4-46c0-4391-9c64-cbb6a366e2dc">IClassActivator</a> interface. This allows <b>IClassActivator</b> to provide access to the class object and instances of the class.

To use class monikers, you must use the <a href="https://msdn.microsoft.com/9361b2c1-ef26-4225-92ff-e0bef0285bc4">CreateClassMoniker</a> function to create these monikers.


<h3><a id="File_Moniker_Implementation"></a><a id="file_moniker_implementation"></a><a id="FILE_MONIKER_IMPLEMENTATION"></a>File Moniker Implementation</h3>
File monikers are monikers that represent a path in the file system; a file moniker can identify any object that is saved in its own file. To identify objects contained within a file, you can compose monikers of other classes (for example, item monikers) to the right of a file moniker. However, the moniker to the left of a file moniker within a composite must be another file moniker, an anti-moniker, or a class moniker. It is illegal, for example, for an item moniker to appear to the left of a file moniker in a composite. 



Note that an anti-moniker is the inverse of an entire file moniker, not the inverse of a component of the path that the moniker represents; that is, when you compose an anti-moniker to the right of a file moniker, the entire file moniker is removed. If you want to remove just the rightmost component of the path represented by a file moniker, you must create a separate file moniker based on the ".." path and then compose that to the end of the file moniker.

A moniker client (using a moniker to get an interface pointer to an object) does not typically need to know the class of the moniker; it can simply call methods using an <b>IMoniker</b> interface pointer.

A moniker provider (handing out monikers that identify its objects to make them accessible to moniker clients) must use file monikers if the objects they are identifying are stored in files. If each object resides in its own file, file monikers are the only type needed. If the objects identified are smaller than a file, you need to use another type of moniker (for example, item monikers) in addition to file monikers.

To use file monikers, you must use the <a href="https://msdn.microsoft.com/d9677fa0-cda0-4b63-a21f-1fd0e27c8f3f">CreateFileMoniker</a> function to create the monikers. To allow your objects to be loaded when a file moniker is bound, your objects must implement the <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a> interface.

The most common example of moniker providers are COM server applications that support linking. If your COM server application supports linking only to file-based documents in their entirety, file monikers are the only type of moniker you need. If your COM server application supports linking to objects smaller than a document (such as sections of a document or embedded objects), you must use item monikers as well as file monikers.

<h3><a id="Generic_Composite_Moniker_Implementation"></a><a id="generic_composite_moniker_implementation"></a><a id="GENERIC_COMPOSITE_MONIKER_IMPLEMENTATION"></a>Generic Composite Moniker Implementation</h3>
A generic composite moniker is a composite moniker whose components have no special knowledge of each other.

Composition is the process of joining two monikers together. Sometimes two monikers of specific classes can be combined in a special manner; for example, a file moniker representing an incomplete path and another file moniker representing a relative path can be combined to form a single file moniker representing the complete path. This is an example of nongeneric composition. Generic composition, on the other hand, can connect any two monikers, no matter what their classes. Because a nongeneric composition depends on the class of the monikers involved, it can be performed only by a particular class's implementation of the <a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">IMoniker::ComposeWith</a> method. You can define new types of nongeneric compositions if you write a new moniker class. By contrast, generic compositions are performed by the <a href="https://msdn.microsoft.com/7fe5b3ff-6e9b-4a28-93d3-52c76d3e8b77">CreateGenericComposite</a> function.

A moniker client (using a moniker to get an interface pointer to an object) does not typically need to know the class of the moniker, or whether it is a generic composite or a nongeneric composite; it can simply call methods using an <b>IMoniker</b> interface pointer.

A moniker provider (handing out monikers that identify its objects to make them accessible to moniker clients) may need to compose two monikers together. (For example, if you are using an item moniker to identify an object, you must compose it with the moniker identifying the object's container before you hand it out.) Use the <a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">IMoniker::ComposeWith</a> method to do this, calling the method on the first moniker and passing the second moniker as a parameter; this method may produce either a generic or a nongeneric composite.

The only time you should explicitly create a generic composite moniker is when you are writing your own moniker class. In your implementation of <a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">IMoniker::ComposeWith</a>h, you should attempt to perform a nongeneric composition whenever possible; if you cannot perform a nongeneric composition and generic composition is acceptable, you can call the <a href="https://msdn.microsoft.com/7fe5b3ff-6e9b-4a28-93d3-52c76d3e8b77">CreateGenericComposite</a> function to create a generic composite moniker.

<h3><a id="Item_Moniker_Implementation"></a><a id="item_moniker_implementation"></a><a id="ITEM_MONIKER_IMPLEMENTATION"></a>Item Moniker Implementation</h3>
Item monikers are used to identify objects within containers, such as a portion of a document, an embedded object within a compound document, or a range of cells within a spreadsheet. Item monikers are often used in combination with file monikers; a file moniker is used to identify the container while an item moniker is used to identify the item within the container.

An item moniker contains a text string; this string is used by the container object to distinguish the contained item from the others. The container object must implement the <a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a> interface; this interface enables the item moniker code to acquire a pointer to an object, given only the string that identifies the object.

A moniker client (using a moniker to get an interface pointer to an object) does not typically need to know the class of the moniker; it simply call methods using an <b>IMoniker</b> interface pointer.

A moniker provider (handing out monikers that identify its objects to make them accessible to moniker clients) must use item monikers if the objects identified are contained within another object and can be individually identified using a string. Use another type of moniker (for example, file monikers) to identify the container object.

To use item monikers, you must use the <a href="https://msdn.microsoft.com/339919ed-660c-4239-825b-7fa96c48e5cd">CreateItemMoniker</a> function to create the monikers. To allow your objects to be loaded when an item moniker is bound, the container of your objects must implement the <a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a> interface.

The most common example of moniker providers are COM applications that support linking. If your COM application supports linking to objects smaller than a file-based document, you need to use item monikers. For a server application that allows linking to a selection within a document, you use the item monikers to identify those objects. For a container application that allows linking to embedded objects, you use the item monikers to identify the embedded objects.

<h3><a id="OBJREF_Moniker_Implementation"></a><a id="objref_moniker_implementation"></a><a id="OBJREF_MONIKER_IMPLEMENTATION"></a>OBJREF Moniker Implementation</h3>
OBJREF monikers represent a reference to an object instance that is running on an out-of-process server, either locally or remotely. The moniker identifies the object instance and the computer the object is running on.

An OBJREF moniker is similar in many ways to a pointer moniker, except that the running object is out-of-process. A client can call <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> on an OBJREF moniker and use the pointer it obtains to access the running object, regardless of its location.

An important distinction from a pointer moniker is that the display name of an OBJREF moniker can be embedded in an HTML page, and the running object represented by the moniker can be bound by a client script, applet, or ActiveX control.

The primary use for an OBJREF moniker is to obtain access to a running object instance over the Internet. An active server page or some other means of generating dynamic HTML content places the display name of an OBJREF moniker in a parameter to an applet or an ActiveX control. The code of the applet or control calls the <a href="https://msdn.microsoft.com/0a214a11-776c-4ef6-af68-a141398f853c">CreateObjrefMoniker</a> function to create an OBJREF moniker based on the display name, and it then calls <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> on the resulting OBJREF moniker to get access to the 
running object instance. The active server page then marshals a pointer to the running object back to the page's client.

<h3><a id="Pointer_Moniker_Implementation"></a><a id="pointer_moniker_implementation"></a><a id="POINTER_MONIKER_IMPLEMENTATION"></a>Pointer Moniker Implementation</h3>
A pointer moniker essentially wraps an interface pointer so that it looks like a moniker and can be passed to those interfaces that require monikers. Binding a pointer moniker is done by calling the pointer's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method.

Instances of pointer monikers refuse to be serialized; that is, <a href="https://msdn.microsoft.com/b748b4f9-ef9c-486b-bdc4-4d23c4640ff7">IPersistStream::Save</a> will return an error. These monikers can, however, be marshaled to a different process in an RPC call; internally, the system marshals and unmarshals the pointer by using the standard paradigm for marshaling interface pointers.





Pointer monikers are rarely needed. Use pointer monikers only if you need monikers to identify objects that have no persistent representation. Pointer monikers allow such objects to participate in a moniker-binding operation.

<h3><a id="URL_Moniker_Implementation"></a><a id="url_moniker_implementation"></a><a id="URL_MONIKER_IMPLEMENTATION"></a>URL Moniker Implementation</h3>
The URL moniker implementation of <b>IMoniker</b> is found on a URL moniker object, which also supports <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and the <a href="_inet_IAsyncMoniker_Interface_cpp">IAsyncMoniker</a> interface. The <b>IMoniker</b> interface inherits its definition from <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> as well as <b>IUnknown</b>, and <b>IPersistStream</b> inherits from <a href="https://msdn.microsoft.com/932eb0e2-35a6-482e-9138-00cff30508a9">IPersist</a>. Therefore, the <b>IMoniker</b> implementation includes support for <b>IPersistStream</b> and <b>IPersist</b>.



The <a href="_inet_IAsyncMoniker_Interface_cpp">IAsyncMoniker</a> interface is simply <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. (There are no additional methods.) It is is used to allow clients to determine whether a moniker supports asynchronous binding.

To get a pointer to the <b>IMoniker</b> interface on this object, call the <b>CreateURLMonikerEx</b> function.

A moniker client (using a moniker to get an interface pointer to an object) does not typically need to know the class of the moniker it is using; it simply calls methods using an <b>IMoniker</b> interface pointer.

A moniker provider (handing out monikers that identify its objects to make them accessible to moniker clients) must use item monikers if the objects it identifies are contained within another object and can be individually identified using a string. It will also need to use another type of moniker (for example, file monikers) to identify the container object.

To use item monikers, you must use the <a href="https://msdn.microsoft.com/339919ed-660c-4239-825b-7fa96c48e5cd">CreateItemMoniker</a> function to create the monikers. To allow your objects to be loaded when an item moniker is bound, the container of
your objects must implement the <a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a> interface.

The most common example of moniker providers are COM applications that support linking. If your COM application supports linking to objects smaller than a file-based documents, you need to use item monikers. For a server application that allows linking to a selection within a document, you use the item monikers to identify those objects. For a container application that allows linking to embedded objects, you use the item monikers to identify the embedded objects. 





## -see-also




<a href="https://msdn.microsoft.com/1f8fcbd6-8f05-4d32-af8a-d8de1b56dacf">CreateAntiMoniker</a>



<a href="https://msdn.microsoft.com/9361b2c1-ef26-4225-92ff-e0bef0285bc4">CreateClassMoniker</a>



<a href="https://msdn.microsoft.com/d9677fa0-cda0-4b63-a21f-1fd0e27c8f3f">CreateFileMoniker</a>



<a href="https://msdn.microsoft.com/7fe5b3ff-6e9b-4a28-93d3-52c76d3e8b77">CreateGenericComposite</a>



<a href="https://msdn.microsoft.com/339919ed-660c-4239-825b-7fa96c48e5cd">CreateItemMoniker</a>



<a href="https://msdn.microsoft.com/0a214a11-776c-4ef6-af68-a141398f853c">CreateObjrefMoniker</a>



<a href="inet_CreateURLMonikerEx_cpp">CreateURLMonikerEx</a>



<a href="https://msdn.microsoft.com/ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b">Monikers</a>
 

 

